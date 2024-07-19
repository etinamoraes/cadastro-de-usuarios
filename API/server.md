import express from 'express'

/*

Criar API

- Criar um usuário;
- Listar todos os usuários;
- Editar Todos os usuários;
- Deletar um usuário;
MongoDB
username: tina_user
Password: rV5qydA9S74Qzwqi

*/

const app = express()
app.use(express.json())

const users = []

app.post('/usuarios', (req, res) => {
 
    users.push(req.body)

    res.status(201).json(req.body)

})

app.get ('/usuarios', (req, res) => {
    res.status(200).json(users)
})

app.listen(3000)