---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241952"
---
# <span data-ttu-id="fb854-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb854-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="fb854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb854-102">SYNOPSIS</span></span>
<span data-ttu-id="fb854-103">Удаляет конфигурацию SQL сервера базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb854-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="fb854-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fb854-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb854-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb854-105">DESCRIPTION</span></span>
<span data-ttu-id="fb854-106">С его SQL сервера базы данных удаляется конфигурация сервера базы данных **Remove-AzSqlServerDisasterRecoveryConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="fb854-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="fb854-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fb854-107">EXAMPLES</span></span>

## <span data-ttu-id="fb854-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb854-108">PARAMETERS</span></span>

### <span data-ttu-id="fb854-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb854-109">-DefaultProfile</span></span>
<span data-ttu-id="fb854-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fb854-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb854-111">-Force</span><span class="sxs-lookup"><span data-stu-id="fb854-111">-Force</span></span>
<span data-ttu-id="fb854-112">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="fb854-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fb854-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb854-113">-ResourceGroupName</span></span>
<span data-ttu-id="fb854-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fb854-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fb854-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fb854-115">-ServerName</span></span>
<span data-ttu-id="fb854-116">Указывает имя сервера SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb854-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="fb854-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="fb854-117">-VirtualEndpointName</span></span>
<span data-ttu-id="fb854-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="fb854-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="fb854-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb854-119">-Confirm</span></span>
<span data-ttu-id="fb854-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb854-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb854-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb854-121">-WhatIf</span></span>
<span data-ttu-id="fb854-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb854-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb854-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fb854-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb854-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb854-124">CommonParameters</span></span>
<span data-ttu-id="fb854-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb854-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb854-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb854-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb854-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb854-127">INPUTS</span></span>

### <span data-ttu-id="fb854-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fb854-128">System.String</span></span>

## <span data-ttu-id="fb854-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fb854-129">OUTPUTS</span></span>

### <span data-ttu-id="fb854-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="fb854-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="fb854-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fb854-131">NOTES</span></span>

## <span data-ttu-id="fb854-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb854-132">RELATED LINKS</span></span>

[<span data-ttu-id="fb854-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb854-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="fb854-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb854-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="fb854-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="fb854-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="fb854-136">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="fb854-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
