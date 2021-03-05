---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a1f91c01d3183551cbabf58754fbe628e1feea32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992393"
---
# <span data-ttu-id="2f295-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f295-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2f295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f295-102">SYNOPSIS</span></span>
<span data-ttu-id="2f295-103">Изменяет конфигурацию сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f295-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="2f295-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f295-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f295-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f295-105">DESCRIPTION</span></span>
<span data-ttu-id="2f295-106">**Cmdlet Set-AzSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f295-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="2f295-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f295-107">EXAMPLES</span></span>

## <span data-ttu-id="2f295-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f295-108">PARAMETERS</span></span>

### <span data-ttu-id="2f295-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="2f295-109">-AllowDataLoss</span></span>
<span data-ttu-id="2f295-110">Указывает на то, что эта операция допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="2f295-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="2f295-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f295-111">-AsJob</span></span>
<span data-ttu-id="2f295-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2f295-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f295-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f295-113">-DefaultProfile</span></span>
<span data-ttu-id="2f295-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2f295-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f295-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="2f295-115">-Failover</span></span>
<span data-ttu-id="2f295-116">Указывает на то, что эта операция является отбойной.</span><span class="sxs-lookup"><span data-stu-id="2f295-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f295-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f295-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f295-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f295-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2f295-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f295-119">-ServerName</span></span>
<span data-ttu-id="2f295-120">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="2f295-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="2f295-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2f295-121">-VirtualEndpointName</span></span>
<span data-ttu-id="2f295-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2f295-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f295-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f295-123">-Confirm</span></span>
<span data-ttu-id="2f295-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2f295-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f295-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f295-125">-WhatIf</span></span>
<span data-ttu-id="2f295-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f295-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f295-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2f295-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f295-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f295-128">CommonParameters</span></span>
<span data-ttu-id="2f295-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f295-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f295-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f295-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f295-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f295-131">INPUTS</span></span>

### <span data-ttu-id="2f295-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2f295-132">System.String</span></span>

## <span data-ttu-id="2f295-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f295-133">OUTPUTS</span></span>

### <span data-ttu-id="2f295-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="2f295-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="2f295-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f295-135">NOTES</span></span>

## <span data-ttu-id="2f295-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f295-136">RELATED LINKS</span></span>

[<span data-ttu-id="2f295-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f295-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f295-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f295-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f295-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f295-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2f295-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="2f295-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
