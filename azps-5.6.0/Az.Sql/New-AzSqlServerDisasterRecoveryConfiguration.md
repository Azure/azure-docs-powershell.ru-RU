---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: e9fd76953d4cf760c501370b77be3301cb043524
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972515"
---
# <span data-ttu-id="7e166-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e166-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="7e166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e166-102">SYNOPSIS</span></span>
<span data-ttu-id="7e166-103">Создает конфигурацию восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e166-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="7e166-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e166-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e166-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e166-105">DESCRIPTION</span></span>
<span data-ttu-id="7e166-106">Для этого создается SQL сервера базы данных **New-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="7e166-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="7e166-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e166-107">EXAMPLES</span></span>

## <span data-ttu-id="7e166-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e166-108">PARAMETERS</span></span>

### <span data-ttu-id="7e166-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e166-109">-AsJob</span></span>
<span data-ttu-id="7e166-110">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e166-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e166-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e166-111">-DefaultProfile</span></span>
<span data-ttu-id="7e166-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e166-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e166-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7e166-113">-FailoverPolicy</span></span>
<span data-ttu-id="7e166-114">Определяет политику отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="7e166-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="7e166-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e166-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7e166-116">Имя группы ресурсов партнера.</span><span class="sxs-lookup"><span data-stu-id="7e166-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="7e166-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="7e166-117">-PartnerServerName</span></span>
<span data-ttu-id="7e166-118">Указывает имя сервера партнера.</span><span class="sxs-lookup"><span data-stu-id="7e166-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="7e166-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e166-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e166-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e166-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7e166-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e166-121">-ServerName</span></span>
<span data-ttu-id="7e166-122">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7e166-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7e166-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="7e166-123">-VirtualEndpointName</span></span>
<span data-ttu-id="7e166-124">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7e166-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="7e166-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e166-125">-Confirm</span></span>
<span data-ttu-id="7e166-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e166-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e166-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e166-127">-WhatIf</span></span>
<span data-ttu-id="7e166-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e166-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e166-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e166-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e166-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e166-130">CommonParameters</span></span>
<span data-ttu-id="7e166-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e166-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e166-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e166-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e166-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e166-133">INPUTS</span></span>

### <span data-ttu-id="7e166-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7e166-134">System.String</span></span>

## <span data-ttu-id="7e166-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e166-135">OUTPUTS</span></span>

### <span data-ttu-id="7e166-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="7e166-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="7e166-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e166-137">NOTES</span></span>

## <span data-ttu-id="7e166-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e166-138">RELATED LINKS</span></span>

[<span data-ttu-id="7e166-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e166-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7e166-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e166-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7e166-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7e166-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7e166-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="7e166-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
