---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerCommunicationLink.md
ms.openlocfilehash: 064262f16a67920b84ca00803325108cc34e6fe5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210836"
---
# <span data-ttu-id="af3e5-101">Remove-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="af3e5-101">Remove-AzSqlServerCommunicationLink</span></span>

## <span data-ttu-id="af3e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af3e5-102">SYNOPSIS</span></span>
<span data-ttu-id="af3e5-103">Удаляет связь для эластичных транзакций базы данных между двумя серверами.</span><span class="sxs-lookup"><span data-stu-id="af3e5-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

## <span data-ttu-id="af3e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af3e5-104">SYNTAX</span></span>

```
Remove-AzSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af3e5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af3e5-105">DESCRIPTION</span></span>
<span data-ttu-id="af3e5-106">С его использованием в azure **SQL** Database удаляется связь между сервером и сервером для транзакций в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="af3e5-106">The **Remove-AzSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="af3e5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af3e5-107">EXAMPLES</span></span>

### <span data-ttu-id="af3e5-108">Пример 1. Удаление связи</span><span class="sxs-lookup"><span data-stu-id="af3e5-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="af3e5-109">Эта команда удаляет связь между сервером и сервером с именем Link01 в ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="af3e5-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="af3e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af3e5-110">PARAMETERS</span></span>

### <span data-ttu-id="af3e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af3e5-111">-DefaultProfile</span></span>
<span data-ttu-id="af3e5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="af3e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af3e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="af3e5-113">-Force</span></span>
<span data-ttu-id="af3e5-114">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="af3e5-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="af3e5-115">-LinkName</span><span class="sxs-lookup"><span data-stu-id="af3e5-115">-LinkName</span></span>
<span data-ttu-id="af3e5-116">Указывает имя сервера, связь с данными которого удаляется этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="af3e5-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="af3e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af3e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="af3e5-118">Имя группы ресурсов, к которой принадлежит сервер, указанный параметром *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="af3e5-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

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

### <span data-ttu-id="af3e5-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af3e5-119">-ServerName</span></span>
<span data-ttu-id="af3e5-120">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="af3e5-120">Specifies the name of a server.</span></span>
<span data-ttu-id="af3e5-121">Этот сервер содержит связь, которую этот cmdlet удаляет.</span><span class="sxs-lookup"><span data-stu-id="af3e5-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="af3e5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af3e5-122">-Confirm</span></span>
<span data-ttu-id="af3e5-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af3e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af3e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af3e5-124">-WhatIf</span></span>
<span data-ttu-id="af3e5-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af3e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af3e5-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af3e5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af3e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af3e5-127">CommonParameters</span></span>
<span data-ttu-id="af3e5-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af3e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af3e5-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="af3e5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af3e5-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af3e5-130">INPUTS</span></span>

### <span data-ttu-id="af3e5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="af3e5-131">System.String</span></span>

## <span data-ttu-id="af3e5-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af3e5-132">OUTPUTS</span></span>

### <span data-ttu-id="af3e5-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="af3e5-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="af3e5-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af3e5-134">NOTES</span></span>
* <span data-ttu-id="af3e5-135">Ключевые слова: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="af3e5-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="af3e5-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af3e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="af3e5-137">Get-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="af3e5-137">Get-AzSqlServerCommunicationLink</span></span>](./Get-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="af3e5-138">New-AzSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="af3e5-138">New-AzSqlServerCommunicationLink</span></span>](./New-AzSqlServerCommunicationLink.md)

[<span data-ttu-id="af3e5-139">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="af3e5-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
