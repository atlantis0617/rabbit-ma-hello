# rabbit-ma-hello
springboot整合rabbitmq

package com.example.demo;

import org.junit.Test;
import org.junit.runner.RunWith;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.test.context.junit4.SpringRunner;

import com.yhy.rabbitmq.RabbitMqHelloApplication;
import com.yhy.rabbitmq.Sender;

@RunWith(SpringRunner.class)
@SpringBootTest(classes=RabbitMqHelloApplication.class)
public class RabbitMqHelloApplicationTests {
	
	@Autowired
	private Sender sender;

	@Test
	public void send() {
		this.sender.send();
	}

}
