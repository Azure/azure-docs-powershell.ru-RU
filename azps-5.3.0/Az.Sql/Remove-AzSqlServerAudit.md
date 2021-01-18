---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerAudit.md
ms.openlocfilehash: ce9bf1a2c7b72e6da92c17e343a993294f8e335d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505859"
---
# <span data-ttu-id="b9377-101">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="b9377-101">Remove-AzSqlServerAudit</span></span>

## <span data-ttu-id="b9377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9377-102">SYNOPSIS</span></span>
<span data-ttu-id="b9377-103">Удаляет параметры аудита для сервера Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b9377-103">Removes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="b9377-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9377-104">SYNTAX</span></span>

### <span data-ttu-id="b9377-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9377-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9377-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9377-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9377-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9377-107">DESCRIPTION</span></span>
<span data-ttu-id="b9377-108">Для **этого с** SQL Azure удаляются параметры аудита.</span><span class="sxs-lookup"><span data-stu-id="b9377-108">The **Remove-AzSqlServerAudit** cmdlet removes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="b9377-109">Укажите *параметры ResourceGroupName* *и ServerName,* чтобы определить сервер.</span><span class="sxs-lookup"><span data-stu-id="b9377-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="b9377-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9377-110">EXAMPLES</span></span>

### <span data-ttu-id="b9377-111">Пример 1. Удаление параметров аудита сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b9377-111">Example 1: Remove the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
```

### <span data-ttu-id="b9377-112">Пример 2. Удаление через канал параметров аудита сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b9377-112">Example 2: Remove, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerAudit
```

## <span data-ttu-id="b9377-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9377-113">PARAMETERS</span></span>

### <span data-ttu-id="b9377-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9377-114">-AsJob</span></span>
<span data-ttu-id="b9377-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9377-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9377-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9377-116">-DefaultProfile</span></span>
<span data-ttu-id="b9377-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9377-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9377-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9377-118">-ResourceGroupName</span></span>
<span data-ttu-id="b9377-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9377-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9377-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9377-120">-ServerName</span></span>
<span data-ttu-id="b9377-121">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b9377-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9377-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="b9377-122">-ServerObject</span></span>
<span data-ttu-id="b9377-123">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="b9377-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9377-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9377-124">-Confirm</span></span>
<span data-ttu-id="b9377-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b9377-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9377-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9377-126">-WhatIf</span></span>
<span data-ttu-id="b9377-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9377-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9377-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9377-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9377-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9377-129">CommonParameters</span></span>
<span data-ttu-id="b9377-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9377-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9377-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9377-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9377-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9377-132">INPUTS</span></span>

### <span data-ttu-id="b9377-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b9377-133">System.String</span></span>

### <span data-ttu-id="b9377-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="b9377-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="b9377-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9377-135">OUTPUTS</span></span>

### <span data-ttu-id="b9377-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9377-136">System.Boolean</span></span>

## <span data-ttu-id="b9377-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9377-137">NOTES</span></span>

## <span data-ttu-id="b9377-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9377-138">RELATED LINKS</span></span>
