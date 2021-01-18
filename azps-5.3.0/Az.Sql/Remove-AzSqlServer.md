---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 068D70EF-39D1-4199-BD74-0EC266DF7072
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServer.md
ms.openlocfilehash: 670b3e6ec71a768fe40bbcf542440db5ec685b2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505860"
---
# <span data-ttu-id="12532-101">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="12532-101">Remove-AzSqlServer</span></span>

## <span data-ttu-id="12532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12532-102">SYNOPSIS</span></span>
<span data-ttu-id="12532-103">Удаляет сервер базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="12532-103">Removes an Azure SQL Database server.</span></span>

## <span data-ttu-id="12532-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12532-104">SYNTAX</span></span>

```
Remove-AzSqlServer [-ServerName] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12532-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12532-105">DESCRIPTION</span></span>
<span data-ttu-id="12532-106">С его использованием удаляется сервер базы данных Azure SQL **AzSqlServer.**</span><span class="sxs-lookup"><span data-stu-id="12532-106">The **Remove-AzSqlServer** cmdlet removes an Azure SQL Database server.</span></span>
<span data-ttu-id="12532-107">Операция удаления является асинхронной и может занять некоторое время, поэтому прежде чем выполнять дополнительные операции, которые зависят от удаления сервера, убедитесь, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="12532-107">The delete operation is asynchronous and may take some time, so verify the operation is finished before performing any additional operations that depend on the server being completely deleted.</span></span>
<span data-ttu-id="12532-108">Например, вам нужно создать сервер с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="12532-108">For instance, you need to create a new server that uses the same name.</span></span>

## <span data-ttu-id="12532-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12532-109">EXAMPLES</span></span>

### <span data-ttu-id="12532-110">Пример 1. Удаление сервера</span><span class="sxs-lookup"><span data-stu-id="12532-110">Example 1: Remove a server</span></span>
```
PS C:\>Remove-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="12532-111">Эта команда удаляет сервер базы данных Azure SQL с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="12532-111">This command removes the Azure SQL Database server named Server01.</span></span>

## <span data-ttu-id="12532-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12532-112">PARAMETERS</span></span>

### <span data-ttu-id="12532-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12532-113">-DefaultProfile</span></span>
<span data-ttu-id="12532-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="12532-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12532-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12532-115">-Force</span></span>
<span data-ttu-id="12532-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="12532-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="12532-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12532-117">-ResourceGroupName</span></span>
<span data-ttu-id="12532-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="12532-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="12532-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="12532-119">-ServerName</span></span>
<span data-ttu-id="12532-120">Имя сервера, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="12532-120">Specifies the name of the server to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12532-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12532-121">-Confirm</span></span>
<span data-ttu-id="12532-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="12532-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12532-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12532-123">-WhatIf</span></span>
<span data-ttu-id="12532-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12532-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12532-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12532-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12532-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12532-126">CommonParameters</span></span>
<span data-ttu-id="12532-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12532-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12532-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12532-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12532-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12532-129">INPUTS</span></span>

### <span data-ttu-id="12532-130">System.String</span><span class="sxs-lookup"><span data-stu-id="12532-130">System.String</span></span>

## <span data-ttu-id="12532-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12532-131">OUTPUTS</span></span>

### <span data-ttu-id="12532-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="12532-132">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="12532-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12532-133">NOTES</span></span>

## <span data-ttu-id="12532-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12532-134">RELATED LINKS</span></span>

[<span data-ttu-id="12532-135">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="12532-135">Get-AzSqlServer</span></span>](./Get-AzSqlServer.md)

[<span data-ttu-id="12532-136">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="12532-136">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="12532-137">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="12532-137">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="12532-138">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="12532-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


