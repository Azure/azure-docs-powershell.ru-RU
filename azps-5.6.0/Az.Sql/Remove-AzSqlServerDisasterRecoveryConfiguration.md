---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 10da2a625eb3858e77343275246d8a142fefc504
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995168"
---
# <span data-ttu-id="4b4c3-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4c3-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="4b4c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4c3-103">Удаляет конфигурацию SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="4b4c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b4c3-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b4c3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b4c3-105">DESCRIPTION</span></span>
<span data-ttu-id="4b4c3-106">С его SQL сервера базы данных удаляется конфигурация сервера базы данных **Remove-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="4b4c3-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="4b4c3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b4c3-107">EXAMPLES</span></span>

## <span data-ttu-id="4b4c3-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b4c3-108">PARAMETERS</span></span>

### <span data-ttu-id="4b4c3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4c3-109">-DefaultProfile</span></span>
<span data-ttu-id="4b4c3-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4b4c3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b4c3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4b4c3-111">-Force</span></span>
<span data-ttu-id="4b4c3-112">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b4c3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4c3-113">-ResourceGroupName</span></span>
<span data-ttu-id="4b4c3-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4b4c3-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b4c3-115">-ServerName</span></span>
<span data-ttu-id="4b4c3-116">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="4b4c3-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="4b4c3-117">-VirtualEndpointName</span></span>
<span data-ttu-id="4b4c3-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b4c3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b4c3-119">-Confirm</span></span>
<span data-ttu-id="4b4c3-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4c3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4c3-121">-WhatIf</span></span>
<span data-ttu-id="4b4c3-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b4c3-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4c3-124">CommonParameters</span></span>
<span data-ttu-id="4b4c3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4c3-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b4c3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4c3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b4c3-127">INPUTS</span></span>

### <span data-ttu-id="4b4c3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4b4c3-128">System.String</span></span>

## <span data-ttu-id="4b4c3-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b4c3-129">OUTPUTS</span></span>

### <span data-ttu-id="4b4c3-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="4b4c3-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="4b4c3-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b4c3-131">NOTES</span></span>

## <span data-ttu-id="4b4c3-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b4c3-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b4c3-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4c3-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4b4c3-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4c3-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4b4c3-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b4c3-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="4b4c3-136">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="4b4c3-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
