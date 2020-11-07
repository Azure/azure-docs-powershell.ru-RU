---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 8f1400ba07444a5fc14d2a3194edd9fe960aaccc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728880"
---
# <span data-ttu-id="2ed02-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed02-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="2ed02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ed02-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed02-103">Создает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="2ed02-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="2ed02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ed02-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ed02-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed02-106">Командлет **New-AzSqlServerDisasterRecoveryConfiguration** создает конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2ed02-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="2ed02-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ed02-107">EXAMPLES</span></span>

## <span data-ttu-id="2ed02-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ed02-108">PARAMETERS</span></span>

### <span data-ttu-id="2ed02-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ed02-109">-AsJob</span></span>
<span data-ttu-id="2ed02-110">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2ed02-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ed02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed02-111">-DefaultProfile</span></span>
<span data-ttu-id="2ed02-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2ed02-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ed02-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="2ed02-113">-FailoverPolicy</span></span>
<span data-ttu-id="2ed02-114">Указывает политику перемещения при сбое.</span><span class="sxs-lookup"><span data-stu-id="2ed02-114">Specifies the failover policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ed02-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed02-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2ed02-116">Указывает имя группы ресурсов для партнеров.</span><span class="sxs-lookup"><span data-stu-id="2ed02-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="2ed02-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2ed02-117">-PartnerServerName</span></span>
<span data-ttu-id="2ed02-118">Указывает имя сервера-партнера.</span><span class="sxs-lookup"><span data-stu-id="2ed02-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="2ed02-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed02-119">-ResourceGroupName</span></span>
<span data-ttu-id="2ed02-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ed02-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2ed02-121">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2ed02-121">-ServerName</span></span>
<span data-ttu-id="2ed02-122">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2ed02-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2ed02-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="2ed02-123">-VirtualEndpointName</span></span>
<span data-ttu-id="2ed02-124">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2ed02-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="2ed02-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ed02-125">-Confirm</span></span>
<span data-ttu-id="2ed02-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ed02-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed02-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed02-127">-WhatIf</span></span>
<span data-ttu-id="2ed02-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ed02-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ed02-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ed02-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed02-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed02-130">CommonParameters</span></span>
<span data-ttu-id="2ed02-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ed02-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed02-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ed02-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed02-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ed02-133">INPUTS</span></span>

### <span data-ttu-id="2ed02-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2ed02-134">System.String</span></span>

## <span data-ttu-id="2ed02-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ed02-135">OUTPUTS</span></span>

### <span data-ttu-id="2ed02-136">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="2ed02-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="2ed02-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ed02-137">NOTES</span></span>

## <span data-ttu-id="2ed02-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ed02-138">RELATED LINKS</span></span>

[<span data-ttu-id="2ed02-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed02-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2ed02-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed02-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2ed02-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed02-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="2ed02-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2ed02-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
