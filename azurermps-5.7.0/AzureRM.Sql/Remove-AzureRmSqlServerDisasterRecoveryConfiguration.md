---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2A74E72B-BD6B-45D7-9C19-B2575C60C43F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 7b5c793bda8b05b78ce97e1f164126de62102fdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563260"
---
# <span data-ttu-id="42dbe-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="42dbe-101">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="42dbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="42dbe-103">Удаляет конфигурацию восстановления системы сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="42dbe-103">Removes a SQL database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42dbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42dbe-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName] <String> [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42dbe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="42dbe-106">Командлет **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** удаляет конфигурацию восстановления системы для сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="42dbe-106">The **Remove-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet removes a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="42dbe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42dbe-107">EXAMPLES</span></span>

## <span data-ttu-id="42dbe-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42dbe-108">PARAMETERS</span></span>

### <span data-ttu-id="42dbe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42dbe-109">-DefaultProfile</span></span>
<span data-ttu-id="42dbe-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="42dbe-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="42dbe-111">-Force</span></span>
<span data-ttu-id="42dbe-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="42dbe-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42dbe-113">-ResourceGroupName</span></span>
<span data-ttu-id="42dbe-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42dbe-114">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="42dbe-115">-ServerName</span></span>
<span data-ttu-id="42dbe-116">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="42dbe-116">Specifies the name of a SQL database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="42dbe-117">-VirtualEndpointName</span></span>
<span data-ttu-id="42dbe-118">Указывает имя виртуальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="42dbe-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42dbe-119">-Confirm</span></span>
<span data-ttu-id="42dbe-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42dbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42dbe-121">-WhatIf</span></span>
<span data-ttu-id="42dbe-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42dbe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42dbe-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42dbe-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42dbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42dbe-124">CommonParameters</span></span>
<span data-ttu-id="42dbe-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42dbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42dbe-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42dbe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42dbe-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42dbe-127">INPUTS</span></span>

### <span data-ttu-id="42dbe-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="42dbe-128">None</span></span>
<span data-ttu-id="42dbe-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="42dbe-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42dbe-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42dbe-130">OUTPUTS</span></span>

## <span data-ttu-id="42dbe-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="42dbe-131">NOTES</span></span>

## <span data-ttu-id="42dbe-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42dbe-132">RELATED LINKS</span></span>

[<span data-ttu-id="42dbe-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="42dbe-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="42dbe-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="42dbe-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="42dbe-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="42dbe-135">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="42dbe-136">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="42dbe-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
