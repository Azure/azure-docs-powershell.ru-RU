---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231713"
---
# <span data-ttu-id="fabb5-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="fabb5-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="fabb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabb5-102">SYNOPSIS</span></span>
<span data-ttu-id="fabb5-103">Удаляет параметры аудита операций поддержки Майкрософт для azure SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="fabb5-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="fabb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fabb5-104">SYNTAX</span></span>

### <span data-ttu-id="fabb5-105">ServerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fabb5-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fabb5-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fabb5-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fabb5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fabb5-107">DESCRIPTION</span></span>
<span data-ttu-id="fabb5-108">Для удаления параметров аудита операций поддержки microsoft для сервера Azure SQL удаляется **cmdlet Remove-AzSqlServerMSSupportAudit.**</span><span class="sxs-lookup"><span data-stu-id="fabb5-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="fabb5-109">Чтобы использовать этот cmdlet, используйте параметры *ResourceGroupName* и *ServerName* для определения сервера.</span><span class="sxs-lookup"><span data-stu-id="fabb5-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="fabb5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fabb5-110">EXAMPLES</span></span>

### <span data-ttu-id="fabb5-111">Пример 1. Удаление параметров аудита операций поддержки Майкрософт для сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="fabb5-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="fabb5-112">Пример 2. Удаление (через конвейер) параметров аудита сервера Azure SQL Майкрософт</span><span class="sxs-lookup"><span data-stu-id="fabb5-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="fabb5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fabb5-113">PARAMETERS</span></span>

### <span data-ttu-id="fabb5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fabb5-114">-AsJob</span></span>
<span data-ttu-id="fabb5-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fabb5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fabb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabb5-116">-DefaultProfile</span></span>
<span data-ttu-id="fabb5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fabb5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fabb5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabb5-118">-ResourceGroupName</span></span>
<span data-ttu-id="fabb5-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fabb5-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="fabb5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fabb5-120">-ServerName</span></span>
<span data-ttu-id="fabb5-121">SQL имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fabb5-121">SQL server name.</span></span>

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

### <span data-ttu-id="fabb5-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="fabb5-122">-ServerObject</span></span>
<span data-ttu-id="fabb5-123">Объект сервера для управления политикой аудита.</span><span class="sxs-lookup"><span data-stu-id="fabb5-123">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="fabb5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fabb5-124">-Confirm</span></span>
<span data-ttu-id="fabb5-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fabb5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fabb5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fabb5-126">-WhatIf</span></span>
<span data-ttu-id="fabb5-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fabb5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fabb5-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fabb5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fabb5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabb5-129">CommonParameters</span></span>
<span data-ttu-id="fabb5-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fabb5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabb5-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fabb5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabb5-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fabb5-132">INPUTS</span></span>

### <span data-ttu-id="fabb5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fabb5-133">System.String</span></span>

### <span data-ttu-id="fabb5-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="fabb5-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="fabb5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fabb5-135">OUTPUTS</span></span>

### <span data-ttu-id="fabb5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fabb5-136">System.Boolean</span></span>

## <span data-ttu-id="fabb5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fabb5-137">NOTES</span></span>

## <span data-ttu-id="fabb5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fabb5-138">RELATED LINKS</span></span>
