Mr. JSON’s life was not that much out of the ordinary, at least for him. The truth was, though, it was quite the opposite. He was popular, even more than his mother — JavaScript. He did not let the popularity go to his head, though. He liked the order, and he was pretty picky about that. In his personal space, everything was organized in a key-value fashion. He took great pride in it and felt he was helping Devity be a better place. He knew humans liked him because of his ease of reading. 
The most peculiar thing about Mr. JSON was that he did not know what he was. OK, he knew he was an object, but after all, he wasn’t a chair or an egg. A human could not touch him. He knew what he was helping do — transferring data was one of many things, but the main. He didn’t know what he was in an absolute sense. He had a body, quite curvy, in his opinion, which he liked. He could hold many things at once, and when he did, he was not letting them go unless commanded the other way. 
He had been meeting with other beings like him. He met, for example, with Mrs. XML. This meeting didn’t go so well, but it is a topic for another story. Let me say they were similar, but an agreement emerged about who was better. It was petty and too much of a drama, but oh well… He was pretty passionate about holding his ground.
Mr. JSON was not a human, not a robot, but a part of the Devity world. He knew he was around 20 human years old, which made him around 40 in the technological world. So as you can see, he had a sense of being, but he was dispersed worldwide and used for different purposes. 
He gladly observed how the Devity developers created a JSON schema and later on decided to make a JSON schema validation. Initially, he was used only when Devity developers made web pages. Now he was pretty powerful, considering he was initially used only to store data. 
His mom told him to watch out for the downsides of fame, but he felt none. Besides, who cared about the downsides? His ego was particularly proud of being a part of JSON Schema validation. Primarily because of his love of order. Maybe it was a little OCD, but the Devity world seemed to appreciate that. 
Devity knew it was essential to know precisely how, for example, a dog record should be organized. The developers needed to know what fields are expected and how the values should be represented. Should a key “isGoodBoy” hold a boolean or a string? The schema validation could verify this question once one was set in place. Also, what should a record look like exactly? This question was the JSON’s schema job to settle. 
Mr. JSON was not limiting anything. He always considered himself an entity that could hold onto a lot. He didn’t mind if the Devity developers stored first and last names together or in two separate keys. Devity knew that this considerable flexibility also carries a great deal of responsibility.
Mr. JSON smiled because he recalled a recent fight between the developers that he ears-dropped. They couldn’t agree on how to represent dog data. The funniest thing was that both of them were thinking that are more right than the other when the truth was both were right. 
This is what the first dev’s dog data looked like:
{
  "dogName": "George",
  "dogType": "dachshund",
  "isGoodBoy": true,
  "birthday": "February 22, 1990",
  "dogHouse": "Berlin, Neukolln, Germany"
}
And this is the set of the second developer:
{
  "dogName": "George",
  "dogType": "dachshund",
  "isGoodBoy": true,
  "birthday": "1990-02-22",
  "address": {
    "city": "Berlin",
    "province": "Neukolln",
    "country": "Germany"
  }
}
There is no right or wrong answer here, as the design of a record will mostly depend on its intended usage inside the application. However, it’s crucial to understand precisely how a record should be structured when an application requests one. Mr. JSON’s Schema steps in to help with that. For the above example, a JSON schema would look like this:
export const activateItemSchema = {
  tags: ['Item'],
  headers: { $ref: 'authorizationSchema#' },
  body: {
    type: 'object',
    required: ['activationCode'],
    properties: {
      activationCode: {
        type: 'string',
        minLength: 7,
        maxLength: 7,
        pattern: '^[A-Z0-9]{3}-[A-Z0-9]{3}$', // activationCode pattern: XXX-XXX
        nullable: false,
      },
    },
    additionalProperties: false,
  },
  params: {
    itemId: {
      type: 'integer',
      minimum: 1,
    },
  },
};
Mr. JSON drifted a bit and started to think if something could be done better when validating. The JSON Schema validation had rules when initialized and was quite blunt with the responses. The schama was either valid or not, with no middle ground. He was also like that. He hated when the developers did not enclose the key names in parentheses. He believed it was made by mistake most of the time, but he always turned red when it happened.
He liked the fact that an empty JSON object is a valid schema. He liked that because he always thought that he existed, so even if empty, he still was there. His presence was noticed, and his ego was tickled by that. In this case, if one passes an empty JSON object as schema validation, one could pass anything there, and all would be valid, like:
7 
"Good dog"
false
{ "numberOfDogs": 7, "dogTraits": ["good", "friendly", "loud"]}
Validating and accepting everything is, of course, not why one would like to have a schema validation in place. Developers most commonly want to restrict received data to a specific type. When you have cat allergies, you do not want to have on your party any furry friends. This is what JSON validation will do for you — not allow any cats to come near you. 

{ "type": "string" }
Will accept only strings, as stated. If a route receives a number type where only a string is supported — the validation will fail. An example might be POST api/
An importand thing to notice is that the JSON schema could also serve as an annotation to the JSON objects. Mr. JSON did have a complex inner life at times, and having this trait was very helpful at times. 


https://www.mongodb.com/docs/manual/core/schema-validation/


