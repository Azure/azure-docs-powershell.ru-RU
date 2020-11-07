---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b3a84fc37e747cb54571bc26563789599fac3a7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906298"
---
# <span data-ttu-id="f9cf9-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9cf9-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="f9cf9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="f9cf9-103">Изменяет конфигурацию восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="f9cf9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9cf9-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9cf9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="f9cf9-106">Командлет **Set-AzSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию восстановления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="f9cf9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9cf9-107">EXAMPLES</span></span>

## <span data-ttu-id="f9cf9-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9cf9-108">PARAMETERS</span></span>

### <span data-ttu-id="f9cf9-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="f9cf9-109">-AllowDataLoss</span></span>
<span data-ttu-id="f9cf9-110">Указывает на то, что операция отработки отказа допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="f9cf9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9cf9-111">-AsJob</span></span>
<span data-ttu-id="f9cf9-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f9cf9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9cf9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9cf9-113">-DefaultProfile</span></span>
<span data-ttu-id="f9cf9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f9cf9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9cf9-115">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="f9cf9-115">-Failover</span></span>
<span data-ttu-id="f9cf9-116">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="f9cf9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9cf9-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9cf9-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f9cf9-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f9cf9-119">-ServerName</span></span>
<span data-ttu-id="f9cf9-120">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="f9cf9-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="f9cf9-121">-VirtualEndpointName</span></span>
<span data-ttu-id="f9cf9-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="f9cf9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9cf9-123">-Confirm</span></span>
<span data-ttu-id="f9cf9-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9cf9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9cf9-125">-WhatIf</span></span>
<span data-ttu-id="f9cf9-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9cf9-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9cf9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9cf9-128">CommonParameters</span></span>
<span data-ttu-id="f9cf9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9cf9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9cf9-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9cf9-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9cf9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9cf9-131">INPUTS</span></span>

### <span data-ttu-id="f9cf9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f9cf9-132">System.String</span></span>

## <span data-ttu-id="f9cf9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9cf9-133">OUTPUTS</span></span>

### <span data-ttu-id="f9cf9-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="f9cf9-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="f9cf9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9cf9-135">NOTES</span></span>

## <span data-ttu-id="f9cf9-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9cf9-136">RELATED LINKS</span></span>

[<span data-ttu-id="f9cf9-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9cf9-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f9cf9-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9cf9-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f9cf9-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9cf9-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="f9cf9-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f9cf9-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
