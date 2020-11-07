---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5bcd5c6317688cc433d83b002cd3cb81ea790aaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732007"
---
# <span data-ttu-id="9dfb6-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9dfb6-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="9dfb6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9dfb6-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfb6-103">Получение целей обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dfb6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9dfb6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dfb6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfb6-105">DESCRIPTION</span></span>
<span data-ttu-id="9dfb6-106">Командлет **Get-AzureRmSqlServerServiceObjective** получает доступные цели обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="9dfb6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9dfb6-107">EXAMPLES</span></span>

### <span data-ttu-id="9dfb6-108">Пример 1: получение целей обслуживания</span><span class="sxs-lookup"><span data-stu-id="9dfb6-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="9dfb6-109">Эта команда получает цели службы для сервера с именем Server01 и базу данных с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="9dfb6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9dfb6-110">PARAMETERS</span></span>

### <span data-ttu-id="9dfb6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dfb6-111">-DatabaseName</span></span>
<span data-ttu-id="9dfb6-112">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-112">SQL Database name.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfb6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfb6-113">-DefaultProfile</span></span>
<span data-ttu-id="9dfb6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9dfb6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dfb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="9dfb6-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9dfb6-117">Этот командлет получает цели службы для сервера базы данных SQL, назначенного этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="9dfb6-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9dfb6-118">-ServerName</span></span>
<span data-ttu-id="9dfb6-119">Указывает имя сервера базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="9dfb6-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9dfb6-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="9dfb6-121">Указывает имя цели обслуживания для сервера базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="9dfb6-122">Допустимые значения этого параметра: Basic, S0, S1, S2, P1, P2 и P3.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dfb6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dfb6-123">-Confirm</span></span>
<span data-ttu-id="9dfb6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dfb6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dfb6-125">-WhatIf</span></span>
<span data-ttu-id="9dfb6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dfb6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dfb6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfb6-128">CommonParameters</span></span>
<span data-ttu-id="9dfb6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfb6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dfb6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfb6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9dfb6-131">INPUTS</span></span>

### <span data-ttu-id="9dfb6-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="9dfb6-132">None</span></span>
<span data-ttu-id="9dfb6-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9dfb6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9dfb6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dfb6-134">OUTPUTS</span></span>

### <span data-ttu-id="9dfb6-135">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="9dfb6-135">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="9dfb6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="9dfb6-136">NOTES</span></span>

## <span data-ttu-id="9dfb6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dfb6-137">RELATED LINKS</span></span>

[<span data-ttu-id="9dfb6-138">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9dfb6-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


