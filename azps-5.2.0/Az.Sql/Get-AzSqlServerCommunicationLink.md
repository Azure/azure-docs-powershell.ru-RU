---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E7E20CD-6A2B-455E-9476-8E0827429162
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 355690129f8edcda2586d2dfee570254ce44d998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406079"
---
# <span data-ttu-id="13a95-101">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a95-101">Get-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="13a95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13a95-102">SYNOPSIS</span></span>
<span data-ttu-id="13a95-103">Возвращает связи для эластичных транзакций базы данных между серверами баз данных.</span><span class="sxs-lookup"><span data-stu-id="13a95-103">Gets communication links for elastic database transactions between database servers.</span></span>

## <span data-ttu-id="13a95-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="13a95-104">SYNTAX</span></span>

```
Get-AzSqlServerCommunicationLink [[-LinkName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13a95-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13a95-105">DESCRIPTION</span></span>
<span data-ttu-id="13a95-106">Для получения связей между серверами и базами данных в базе данных SQL Azure для передачи данных между серверами и серверами возвращается **cmdlet Get-AzSqlServerCommunicationLink.**</span><span class="sxs-lookup"><span data-stu-id="13a95-106">The **Get-AzSqlServerCommunicationLink** cmdlet gets server-to-server communication links for elastic database transactions in Azure SQL Database.</span></span>
<span data-ttu-id="13a95-107">Укажите имя связи с сервером, чтобы увидеть свойства этой ссылки.</span><span class="sxs-lookup"><span data-stu-id="13a95-107">Specify the name of a server communication link to see the properties for that link.</span></span>

## <span data-ttu-id="13a95-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="13a95-108">EXAMPLES</span></span>

### <span data-ttu-id="13a95-109">Пример 1. Получить все коммуникационные ссылки для сервера</span><span class="sxs-lookup"><span data-stu-id="13a95-109">Example 1: Get all communication links for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17"
```

<span data-ttu-id="13a95-110">Эта команда получает все связи между сервером и сервером для эластичных транзакций базы данных для сервера ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="13a95-110">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17.</span></span>

### <span data-ttu-id="13a95-111">Пример 2. Получить связь для сервера</span><span class="sxs-lookup"><span data-stu-id="13a95-111">Example 2: Get a specific communication link for a server</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="13a95-112">Эта команда получает связь между сервером и сервером с именем Link01.</span><span class="sxs-lookup"><span data-stu-id="13a95-112">This command gets the server-to-server communication link named Link01.</span></span>

### <span data-ttu-id="13a95-113">Пример 3. Получить все коммуникационные ссылки для сервера с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="13a95-113">Example 3: Get all communication links for a server using filtering</span></span>
```
PS C:\> Get-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link*"
```

<span data-ttu-id="13a95-114">Эта команда получает все связи между сервером и сервером для эластичных транзакций базы данных для сервера ContosoServer17, которые начинаются с "Ссылка".</span><span class="sxs-lookup"><span data-stu-id="13a95-114">This command gets all server-to-server communication links for elastic database transactions for the server named ContosoServer17 that start with "Link".</span></span>

## <span data-ttu-id="13a95-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13a95-115">PARAMETERS</span></span>

### <span data-ttu-id="13a95-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13a95-116">-DefaultProfile</span></span>
<span data-ttu-id="13a95-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="13a95-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13a95-118">-LinkName</span><span class="sxs-lookup"><span data-stu-id="13a95-118">-LinkName</span></span>
<span data-ttu-id="13a95-119">Указывает имя серверной связи, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13a95-119">Specifies the name of the server communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13a95-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13a95-120">-ResourceGroupName</span></span>
<span data-ttu-id="13a95-121">Имя группы ресурсов, к которой принадлежит сервер, указанный параметром *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="13a95-121">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="13a95-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="13a95-122">-ServerName</span></span>
<span data-ttu-id="13a95-123">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="13a95-123">Specifies the name of a server.</span></span>
<span data-ttu-id="13a95-124">Этот сервер содержит связь, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13a95-124">This server contains a communication link that this cmdlet gets.</span></span>

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

### <span data-ttu-id="13a95-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13a95-125">-Confirm</span></span>
<span data-ttu-id="13a95-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="13a95-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13a95-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13a95-127">-WhatIf</span></span>
<span data-ttu-id="13a95-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13a95-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13a95-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="13a95-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13a95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13a95-130">CommonParameters</span></span>
<span data-ttu-id="13a95-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13a95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13a95-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13a95-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13a95-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13a95-133">INPUTS</span></span>

### <span data-ttu-id="13a95-134">System.String</span><span class="sxs-lookup"><span data-stu-id="13a95-134">System.String</span></span>

## <span data-ttu-id="13a95-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="13a95-135">OUTPUTS</span></span>

### <span data-ttu-id="13a95-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="13a95-136">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="13a95-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="13a95-137">NOTES</span></span>
* <span data-ttu-id="13a95-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="13a95-138">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="13a95-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13a95-139">RELATED LINKS</span></span>

[<span data-ttu-id="13a95-140">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a95-140">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="13a95-141">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="13a95-141">Remove-AzSqlServerCommunicationLink</span></span>](./Remove-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="13a95-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="13a95-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
