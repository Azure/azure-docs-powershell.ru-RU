---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408116"
---
# <span data-ttu-id="6a236-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a236-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="6a236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a236-102">SYNOPSIS</span></span>
<span data-ttu-id="6a236-103">Изменяет конфигурацию сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a236-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="6a236-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a236-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a236-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a236-105">DESCRIPTION</span></span>
<span data-ttu-id="6a236-106">**Cmdlet Set-AzSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a236-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="6a236-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a236-107">EXAMPLES</span></span>

## <span data-ttu-id="6a236-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a236-108">PARAMETERS</span></span>

### <span data-ttu-id="6a236-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="6a236-109">-AllowDataLoss</span></span>
<span data-ttu-id="6a236-110">Указывает на то, что эта операция допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="6a236-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="6a236-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a236-111">-AsJob</span></span>
<span data-ttu-id="6a236-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a236-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a236-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a236-113">-DefaultProfile</span></span>
<span data-ttu-id="6a236-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6a236-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a236-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="6a236-115">-Failover</span></span>
<span data-ttu-id="6a236-116">Указывает на то, что эта операция является отбойной.</span><span class="sxs-lookup"><span data-stu-id="6a236-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="6a236-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a236-117">-ResourceGroupName</span></span>
<span data-ttu-id="6a236-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6a236-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6a236-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a236-119">-ServerName</span></span>
<span data-ttu-id="6a236-120">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="6a236-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="6a236-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="6a236-121">-VirtualEndpointName</span></span>
<span data-ttu-id="6a236-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6a236-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="6a236-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a236-123">-Confirm</span></span>
<span data-ttu-id="6a236-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6a236-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a236-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a236-125">-WhatIf</span></span>
<span data-ttu-id="6a236-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a236-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a236-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a236-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a236-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a236-128">CommonParameters</span></span>
<span data-ttu-id="6a236-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a236-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a236-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a236-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a236-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a236-131">INPUTS</span></span>

### <span data-ttu-id="6a236-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6a236-132">System.String</span></span>

## <span data-ttu-id="6a236-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a236-133">OUTPUTS</span></span>

### <span data-ttu-id="6a236-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="6a236-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="6a236-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a236-135">NOTES</span></span>

## <span data-ttu-id="6a236-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a236-136">RELATED LINKS</span></span>

[<span data-ttu-id="6a236-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a236-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6a236-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a236-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6a236-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a236-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="6a236-140">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="6a236-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
