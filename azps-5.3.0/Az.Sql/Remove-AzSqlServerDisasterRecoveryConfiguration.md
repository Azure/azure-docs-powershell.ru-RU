---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504781"
---
# <span data-ttu-id="0216c-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0216c-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="0216c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0216c-102">SYNOPSIS</span></span>
<span data-ttu-id="0216c-103">Удаляет конфигурацию SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="0216c-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="0216c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0216c-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0216c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0216c-105">DESCRIPTION</span></span>
<span data-ttu-id="0216c-106">С его SQL сервера базы данных удаляется конфигурация сервера базы данных **Remove-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="0216c-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="0216c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0216c-107">EXAMPLES</span></span>

## <span data-ttu-id="0216c-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0216c-108">PARAMETERS</span></span>

### <span data-ttu-id="0216c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0216c-109">-DefaultProfile</span></span>
<span data-ttu-id="0216c-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0216c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0216c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0216c-111">-Force</span></span>
<span data-ttu-id="0216c-112">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0216c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0216c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0216c-113">-ResourceGroupName</span></span>
<span data-ttu-id="0216c-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0216c-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0216c-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0216c-115">-ServerName</span></span>
<span data-ttu-id="0216c-116">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="0216c-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="0216c-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="0216c-117">-VirtualEndpointName</span></span>
<span data-ttu-id="0216c-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0216c-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="0216c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0216c-119">-Confirm</span></span>
<span data-ttu-id="0216c-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0216c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0216c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0216c-121">-WhatIf</span></span>
<span data-ttu-id="0216c-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0216c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0216c-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0216c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0216c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0216c-124">CommonParameters</span></span>
<span data-ttu-id="0216c-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0216c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0216c-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0216c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0216c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0216c-127">INPUTS</span></span>

### <span data-ttu-id="0216c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0216c-128">System.String</span></span>

## <span data-ttu-id="0216c-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0216c-129">OUTPUTS</span></span>

### <span data-ttu-id="0216c-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="0216c-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="0216c-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0216c-131">NOTES</span></span>

## <span data-ttu-id="0216c-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0216c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0216c-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0216c-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0216c-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0216c-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0216c-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="0216c-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="0216c-136">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="0216c-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
