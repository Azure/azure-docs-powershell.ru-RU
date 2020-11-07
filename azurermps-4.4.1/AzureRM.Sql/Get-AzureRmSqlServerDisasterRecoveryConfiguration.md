---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: bbb6841f615444175de93e59d4536a07461490de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733606"
---
# <span data-ttu-id="08cc6-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08cc6-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="08cc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="08cc6-103">Возвращает конфигурацию восстановления системы сервера баз данных.</span><span class="sxs-lookup"><span data-stu-id="08cc6-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08cc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08cc6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08cc6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="08cc6-106">Командлет **Get-AzureRmSqlServerDisasterRecoveryConfiguration** возвращает конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="08cc6-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="08cc6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08cc6-107">EXAMPLES</span></span>

## <span data-ttu-id="08cc6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08cc6-108">PARAMETERS</span></span>

### <span data-ttu-id="08cc6-109">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08cc6-109">-ResourceGroupName</span></span>
<span data-ttu-id="08cc6-110">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="08cc6-110">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="08cc6-111">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="08cc6-111">-ServerName</span></span>
<span data-ttu-id="08cc6-112">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="08cc6-112">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="08cc6-113">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="08cc6-113">-VirtualEndpointName</span></span>
<span data-ttu-id="08cc6-114">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="08cc6-114">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="08cc6-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08cc6-115">-Confirm</span></span>
<span data-ttu-id="08cc6-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08cc6-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08cc6-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08cc6-117">-WhatIf</span></span>
<span data-ttu-id="08cc6-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08cc6-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08cc6-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08cc6-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08cc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cc6-120">-DefaultProfile</span></span>
<span data-ttu-id="08cc6-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08cc6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08cc6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cc6-122">CommonParameters</span></span>
<span data-ttu-id="08cc6-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08cc6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cc6-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cc6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cc6-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08cc6-125">INPUTS</span></span>

## <span data-ttu-id="08cc6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08cc6-126">OUTPUTS</span></span>

## <span data-ttu-id="08cc6-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="08cc6-127">NOTES</span></span>

## <span data-ttu-id="08cc6-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08cc6-128">RELATED LINKS</span></span>

[<span data-ttu-id="08cc6-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08cc6-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08cc6-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08cc6-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08cc6-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="08cc6-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="08cc6-132">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="08cc6-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

