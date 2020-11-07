---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 63bfce9b6f0d6aaa97fede65d8c96ac9079be349
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734752"
---
# <span data-ttu-id="3efd2-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3efd2-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="3efd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3efd2-102">SYNOPSIS</span></span>
<span data-ttu-id="3efd2-103">Удаляет связь для транзакций эластичных баз данных между двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="3efd2-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3efd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3efd2-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3efd2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3efd2-105">DESCRIPTION</span></span>
<span data-ttu-id="3efd2-106">Командлет **Remove-AzureRmSqlServerCommunicationLink** удаляет связь "сервер-сервер" для транзакций эластичных баз данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3efd2-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="3efd2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3efd2-107">EXAMPLES</span></span>

### <span data-ttu-id="3efd2-108">Пример 1: удаление коммуникационной ссылки</span><span class="sxs-lookup"><span data-stu-id="3efd2-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="3efd2-109">Эта команда удаляет связь "сервер-сервер" с именем Link01 на ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="3efd2-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="3efd2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3efd2-110">PARAMETERS</span></span>

### <span data-ttu-id="3efd2-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3efd2-111">-Force</span></span>
<span data-ttu-id="3efd2-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3efd2-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-113">-LinkName</span><span class="sxs-lookup"><span data-stu-id="3efd2-113">-LinkName</span></span>
<span data-ttu-id="3efd2-114">Указывает имя связи сервера, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3efd2-114">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3efd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="3efd2-116">Указывает имя группы ресурсов, к которой принадлежит сервер, указанный в параметре *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="3efd2-116">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3efd2-117">-ServerName</span></span>
<span data-ttu-id="3efd2-118">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3efd2-118">Specifies the name of a server.</span></span>
<span data-ttu-id="3efd2-119">Этот сервер включает ссылку для связи, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3efd2-119">This server contains the communication link that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3efd2-120">-Confirm</span></span>
<span data-ttu-id="3efd2-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3efd2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3efd2-122">-WhatIf</span></span>
<span data-ttu-id="3efd2-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3efd2-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3efd2-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3efd2-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3efd2-125">-DefaultProfile</span></span>
<span data-ttu-id="3efd2-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3efd2-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3efd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3efd2-127">CommonParameters</span></span>
<span data-ttu-id="3efd2-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3efd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3efd2-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3efd2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3efd2-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3efd2-130">INPUTS</span></span>

## <span data-ttu-id="3efd2-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3efd2-131">OUTPUTS</span></span>

### <span data-ttu-id="3efd2-132">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="3efd2-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="3efd2-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3efd2-133">NOTES</span></span>
* <span data-ttu-id="3efd2-134">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, SQL, база данных и MSSQL</span><span class="sxs-lookup"><span data-stu-id="3efd2-134">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3efd2-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3efd2-135">RELATED LINKS</span></span>

[<span data-ttu-id="3efd2-136">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3efd2-136">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="3efd2-137">New-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="3efd2-137">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="3efd2-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3efd2-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
