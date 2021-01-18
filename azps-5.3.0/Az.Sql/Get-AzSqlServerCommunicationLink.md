---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508038"
---
# <span data-ttu-id="45e6a-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="45e6a-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="45e6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="45e6a-103">Возвращает коммуникационные связи для транзакций с эластичными базами данных между серверами баз данных.</span><span class="sxs-lookup"><span data-stu-id="45e6a-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="45e6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45e6a-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45e6a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="45e6a-106">С использованием cmdlet **Get-AzSqlServerCommunicationLink** можно получить связи между серверами и серверами для эластичных транзакций базы данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="45e6a-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="45e6a-107">Укажите имя связи с сервером, чтобы увидеть свойства этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="45e6a-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="45e6a-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45e6a-108">EXAMPLES</span></span>

### <span data-ttu-id="45e6a-109">Пример 1. Получить все коммуникационные ссылки для сервера</span><span class="sxs-lookup"><span data-stu-id="45e6a-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="45e6a-110">Эта команда получает все связи между сервером и сервером для эластичных транзакций базы данных для сервера ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="45e6a-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="45e6a-111">Пример 2. Получить связь для сервера</span><span class="sxs-lookup"><span data-stu-id="45e6a-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="45e6a-112">Эта команда получает связь между сервером и сервером с именем Link01.</span><span class="sxs-lookup"><span data-stu-id="45e6a-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="45e6a-113">Пример 3. Получить все коммуникационные ссылки для сервера с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="45e6a-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="45e6a-114">Эта команда получает все связи между сервером и сервером для эластичных транзакций базы данных для сервера ContosoServer17, которые начинаются с "Ссылка".</span><span class="sxs-lookup"><span data-stu-id="45e6a-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="45e6a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45e6a-115">PARAMETERS</span></span>

### <span data-ttu-id="45e6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e6a-116">-DefaultProfile</span></span>
<span data-ttu-id="45e6a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="45e6a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45e6a-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="45e6a-118">-LinkName</span></span>
<span data-ttu-id="45e6a-119">Указывает имя серверной связи, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e6a-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45e6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="45e6a-121">Имя группы ресурсов, к которой принадлежит сервер, указанный *параметром ServerName.*</span><span class="sxs-lookup"><span data-stu-id="45e6a-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="45e6a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="45e6a-122">-ServerName</span></span>
<span data-ttu-id="45e6a-123">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="45e6a-123">Specifies the name of a server.</span></span>
<span data-ttu-id="45e6a-124">Этот сервер содержит связь, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e6a-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="45e6a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45e6a-125">-Confirm</span></span>
<span data-ttu-id="45e6a-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="45e6a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e6a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e6a-127">-WhatIf</span></span>
<span data-ttu-id="45e6a-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e6a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e6a-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45e6a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e6a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e6a-130">CommonParameters</span></span>
<span data-ttu-id="45e6a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e6a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e6a-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45e6a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e6a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45e6a-133">INPUTS</span></span>

### <span data-ttu-id="45e6a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="45e6a-134">System.String</span></span>

## <span data-ttu-id="45e6a-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45e6a-135">OUTPUTS</span></span>

### <span data-ttu-id="45e6a-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="45e6a-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="45e6a-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45e6a-137">NOTES</span></span>
* <span data-ttu-id="45e6a-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="45e6a-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="45e6a-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45e6a-139">RELATED LINKS</span></span>

[<span data-ttu-id="45e6a-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="45e6a-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="45e6a-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="45e6a-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="45e6a-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="45e6a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
