---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395676"
---
# <span data-ttu-id="7d686-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d686-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="7d686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d686-102">SYNOPSIS</span></span>
<span data-ttu-id="7d686-103">Создает конфигурацию восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="7d686-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="7d686-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d686-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d686-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d686-105">DESCRIPTION</span></span>
<span data-ttu-id="7d686-106">Для этого создается SQL сервера базы данных **New-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="7d686-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="7d686-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d686-107">EXAMPLES</span></span>

## <span data-ttu-id="7d686-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d686-108">PARAMETERS</span></span>

### <span data-ttu-id="7d686-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d686-109">-AsJob</span></span>
<span data-ttu-id="7d686-110">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7d686-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d686-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d686-111">-DefaultProfile</span></span>
<span data-ttu-id="7d686-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d686-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d686-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7d686-113">-FailoverPolicy</span></span>
<span data-ttu-id="7d686-114">Определяет политику отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="7d686-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="7d686-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d686-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7d686-116">Имя группы ресурсов партнера.</span><span class="sxs-lookup"><span data-stu-id="7d686-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="7d686-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="7d686-117">-PartnerServerName</span></span>
<span data-ttu-id="7d686-118">Указывает имя сервера партнера.</span><span class="sxs-lookup"><span data-stu-id="7d686-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="7d686-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d686-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d686-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d686-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7d686-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7d686-121">-ServerName</span></span>
<span data-ttu-id="7d686-122">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="7d686-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="7d686-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="7d686-123">-VirtualEndpointName</span></span>
<span data-ttu-id="7d686-124">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="7d686-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="7d686-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d686-125">-Confirm</span></span>
<span data-ttu-id="7d686-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d686-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d686-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d686-127">-WhatIf</span></span>
<span data-ttu-id="7d686-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d686-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d686-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7d686-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d686-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d686-130">CommonParameters</span></span>
<span data-ttu-id="7d686-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d686-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d686-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d686-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d686-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d686-133">INPUTS</span></span>

### <span data-ttu-id="7d686-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7d686-134">System.String</span></span>

## <span data-ttu-id="7d686-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d686-135">OUTPUTS</span></span>

### <span data-ttu-id="7d686-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="7d686-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="7d686-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d686-137">NOTES</span></span>

## <span data-ttu-id="7d686-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d686-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d686-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d686-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7d686-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d686-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7d686-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="7d686-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="7d686-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="7d686-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
