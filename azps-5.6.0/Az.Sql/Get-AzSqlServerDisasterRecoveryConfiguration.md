---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: ad00759bb2babb85c17ab9efe2d7e47025434607
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982035"
---
# <span data-ttu-id="e4c46-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4c46-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="e4c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c46-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c46-103">Получает конфигурацию восстановления системы сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4c46-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="e4c46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4c46-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4c46-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4c46-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c46-106">Для этого требуется SQL сервера базы данных **Get-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="e4c46-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="e4c46-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4c46-107">EXAMPLES</span></span>

## <span data-ttu-id="e4c46-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4c46-108">PARAMETERS</span></span>

### <span data-ttu-id="e4c46-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c46-109">-DefaultProfile</span></span>
<span data-ttu-id="e4c46-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e4c46-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4c46-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c46-111">-ResourceGroupName</span></span>
<span data-ttu-id="e4c46-112">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e4c46-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e4c46-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e4c46-113">-ServerName</span></span>
<span data-ttu-id="e4c46-114">Указывает имя SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e4c46-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="e4c46-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="e4c46-115">-VirtualEndpointName</span></span>
<span data-ttu-id="e4c46-116">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e4c46-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="e4c46-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4c46-117">-Confirm</span></span>
<span data-ttu-id="e4c46-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c46-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c46-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c46-119">-WhatIf</span></span>
<span data-ttu-id="e4c46-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4c46-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c46-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4c46-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c46-122">CommonParameters</span></span>
<span data-ttu-id="e4c46-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4c46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c46-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4c46-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c46-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4c46-125">INPUTS</span></span>

### <span data-ttu-id="e4c46-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e4c46-126">System.String</span></span>

## <span data-ttu-id="e4c46-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4c46-127">OUTPUTS</span></span>

### <span data-ttu-id="e4c46-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="e4c46-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="e4c46-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4c46-129">NOTES</span></span>

## <span data-ttu-id="e4c46-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4c46-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4c46-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4c46-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e4c46-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4c46-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e4c46-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4c46-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="e4c46-134">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="e4c46-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

