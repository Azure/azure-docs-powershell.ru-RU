---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: c49eb386265dff2650ba9bdb0882d25be98fca0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243859"
---
# <span data-ttu-id="5da8d-101">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da8d-101">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="5da8d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5da8d-102">SYNOPSIS</span></span>
<span data-ttu-id="5da8d-103">Изменяет конфигурацию восстановления сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="5da8d-103">Modifies a database server recovery configuration.</span></span>

## <span data-ttu-id="5da8d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5da8d-104">SYNTAX</span></span>

```
Set-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5da8d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5da8d-105">DESCRIPTION</span></span>
<span data-ttu-id="5da8d-106">Командлет **Set-AzSqlServerDisasterRecoveryConfiguration** изменяет конфигурацию восстановления сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5da8d-106">The **Set-AzSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="5da8d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5da8d-107">EXAMPLES</span></span>

## <span data-ttu-id="5da8d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5da8d-108">PARAMETERS</span></span>

### <span data-ttu-id="5da8d-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5da8d-109">-AllowDataLoss</span></span>
<span data-ttu-id="5da8d-110">Указывает на то, что операция отработки отказа допускает потерю данных.</span><span class="sxs-lookup"><span data-stu-id="5da8d-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="5da8d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5da8d-111">-AsJob</span></span>
<span data-ttu-id="5da8d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5da8d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5da8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da8d-113">-DefaultProfile</span></span>
<span data-ttu-id="5da8d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5da8d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5da8d-115">-Отработка отказа</span><span class="sxs-lookup"><span data-stu-id="5da8d-115">-Failover</span></span>
<span data-ttu-id="5da8d-116">Указывает на то, что эта операция является отказоустойчивым.</span><span class="sxs-lookup"><span data-stu-id="5da8d-116">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="5da8d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da8d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5da8d-118">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5da8d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5da8d-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5da8d-119">-ServerName</span></span>
<span data-ttu-id="5da8d-120">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5da8d-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="5da8d-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="5da8d-121">-VirtualEndpointName</span></span>
<span data-ttu-id="5da8d-122">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="5da8d-122">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="5da8d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5da8d-123">-Confirm</span></span>
<span data-ttu-id="5da8d-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5da8d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5da8d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5da8d-125">-WhatIf</span></span>
<span data-ttu-id="5da8d-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5da8d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5da8d-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5da8d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5da8d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da8d-128">CommonParameters</span></span>
<span data-ttu-id="5da8d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5da8d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da8d-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5da8d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da8d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5da8d-131">INPUTS</span></span>

### <span data-ttu-id="5da8d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5da8d-132">System.String</span></span>

## <span data-ttu-id="5da8d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5da8d-133">OUTPUTS</span></span>

### <span data-ttu-id="5da8d-134">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="5da8d-134">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="5da8d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5da8d-135">NOTES</span></span>

## <span data-ttu-id="5da8d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5da8d-136">RELATED LINKS</span></span>

[<span data-ttu-id="5da8d-137">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da8d-137">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5da8d-138">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da8d-138">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5da8d-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da8d-139">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="5da8d-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5da8d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
