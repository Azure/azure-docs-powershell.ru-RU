---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: df3ed9faa96a98b4e94df370bf90161e7baf2b99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072938"
---
# <span data-ttu-id="3007b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3007b-101">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="3007b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3007b-102">SYNOPSIS</span></span>
<span data-ttu-id="3007b-103">Удаляет конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3007b-103">Removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="3007b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3007b-104">SYNTAX</span></span>

```
Remove-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3007b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3007b-105">DESCRIPTION</span></span>
<span data-ttu-id="3007b-106">Командлет **Remove-AzSqlServerDisasterRecoveryConfiguration** удаляет конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3007b-106">The **Remove-AzSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="3007b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3007b-107">EXAMPLES</span></span>

## <span data-ttu-id="3007b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3007b-108">PARAMETERS</span></span>

### <span data-ttu-id="3007b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3007b-109">-DefaultProfile</span></span>
<span data-ttu-id="3007b-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3007b-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3007b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3007b-111">-Force</span></span>
<span data-ttu-id="3007b-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3007b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3007b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3007b-113">-ResourceGroupName</span></span>
<span data-ttu-id="3007b-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3007b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3007b-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3007b-115">-ServerName</span></span>
<span data-ttu-id="3007b-116">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3007b-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="3007b-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="3007b-117">-VirtualEndpointName</span></span>
<span data-ttu-id="3007b-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3007b-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="3007b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3007b-119">-Confirm</span></span>
<span data-ttu-id="3007b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3007b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3007b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3007b-121">-WhatIf</span></span>
<span data-ttu-id="3007b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3007b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3007b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3007b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3007b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3007b-124">CommonParameters</span></span>
<span data-ttu-id="3007b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3007b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3007b-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3007b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3007b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3007b-127">INPUTS</span></span>

### <span data-ttu-id="3007b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3007b-128">System.String</span></span>

## <span data-ttu-id="3007b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3007b-129">OUTPUTS</span></span>

### <span data-ttu-id="3007b-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="3007b-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="3007b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3007b-131">NOTES</span></span>

## <span data-ttu-id="3007b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3007b-132">RELATED LINKS</span></span>

[<span data-ttu-id="3007b-133">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3007b-133">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3007b-134">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3007b-134">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3007b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3007b-135">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3007b-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3007b-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
