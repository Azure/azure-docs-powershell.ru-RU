---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 3b5a512e5c301e328bf556d63d7ecb9191a08c5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734594"
---
# <span data-ttu-id="3eebf-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eebf-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="3eebf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3eebf-102">SYNOPSIS</span></span>
<span data-ttu-id="3eebf-103">Удаляет конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3eebf-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eebf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3eebf-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eebf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eebf-105">DESCRIPTION</span></span>
<span data-ttu-id="3eebf-106">Командлет **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** удаляет конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3eebf-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="3eebf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3eebf-107">EXAMPLES</span></span>

## <span data-ttu-id="3eebf-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3eebf-108">PARAMETERS</span></span>

### <span data-ttu-id="3eebf-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eebf-109">-DefaultProfile</span></span>
<span data-ttu-id="3eebf-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3eebf-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eebf-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3eebf-111">-Force</span></span>
<span data-ttu-id="3eebf-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="3eebf-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3eebf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eebf-113">-ResourceGroupName</span></span>
<span data-ttu-id="3eebf-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3eebf-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3eebf-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3eebf-115">-ServerName</span></span>
<span data-ttu-id="3eebf-116">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="3eebf-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="3eebf-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="3eebf-117">-VirtualEndpointName</span></span>
<span data-ttu-id="3eebf-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3eebf-118">Specifies the name of a virtual end point.</span></span>

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

### <span data-ttu-id="3eebf-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eebf-119">-Confirm</span></span>
<span data-ttu-id="3eebf-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3eebf-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eebf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eebf-121">-WhatIf</span></span>
<span data-ttu-id="3eebf-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3eebf-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eebf-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3eebf-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eebf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eebf-124">CommonParameters</span></span>
<span data-ttu-id="3eebf-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3eebf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eebf-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eebf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eebf-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3eebf-127">INPUTS</span></span>

### <span data-ttu-id="3eebf-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3eebf-128">System.String</span></span>

## <span data-ttu-id="3eebf-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3eebf-129">OUTPUTS</span></span>

### <span data-ttu-id="3eebf-130">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="3eebf-130">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="3eebf-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3eebf-131">NOTES</span></span>

## <span data-ttu-id="3eebf-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3eebf-132">RELATED LINKS</span></span>

[<span data-ttu-id="3eebf-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eebf-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3eebf-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eebf-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3eebf-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eebf-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3eebf-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="3eebf-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
