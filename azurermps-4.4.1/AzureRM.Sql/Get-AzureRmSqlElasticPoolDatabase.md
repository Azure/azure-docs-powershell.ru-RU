---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562035"
---
# <span data-ttu-id="2a67e-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="2a67e-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="2a67e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a67e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a67e-103">Возвращает эластичные базы данных в пуле эластичных БД и их значения свойств.</span><span class="sxs-lookup"><span data-stu-id="2a67e-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a67e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a67e-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a67e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a67e-105">DESCRIPTION</span></span>
<span data-ttu-id="2a67e-106">Командлет **Get-AzureRmSqlElasticPoolDatabase** получает эластичные базы данных в пуле эластичных БД и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="2a67e-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="2a67e-107">В базе данных SQL Azure можно указать имя эластичной базы данных, чтобы просмотреть значения свойств только для этой базы данных.</span><span class="sxs-lookup"><span data-stu-id="2a67e-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="2a67e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a67e-108">EXAMPLES</span></span>

### <span data-ttu-id="2a67e-109">Пример 1: получение всех баз данных в пуле эластичных БД</span><span class="sxs-lookup"><span data-stu-id="2a67e-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="2a67e-110">Эта команда получает все базы данных в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="2a67e-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="2a67e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a67e-111">PARAMETERS</span></span>

### <span data-ttu-id="2a67e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2a67e-112">-DatabaseName</span></span>
<span data-ttu-id="2a67e-113">Указывает имя базы данных SQL, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2a67e-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a67e-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2a67e-114">-ElasticPoolName</span></span>
<span data-ttu-id="2a67e-115">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="2a67e-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="2a67e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a67e-116">-ResourceGroupName</span></span>
<span data-ttu-id="2a67e-117">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="2a67e-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="2a67e-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2a67e-118">-ServerName</span></span>
<span data-ttu-id="2a67e-119">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="2a67e-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="2a67e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a67e-120">-Confirm</span></span>
<span data-ttu-id="2a67e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a67e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a67e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a67e-122">-WhatIf</span></span>
<span data-ttu-id="2a67e-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a67e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a67e-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a67e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a67e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a67e-125">-DefaultProfile</span></span>
<span data-ttu-id="2a67e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a67e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a67e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a67e-127">CommonParameters</span></span>
<span data-ttu-id="2a67e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a67e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a67e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a67e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a67e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a67e-130">INPUTS</span></span>

## <span data-ttu-id="2a67e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a67e-131">OUTPUTS</span></span>

### <span data-ttu-id="2a67e-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="2a67e-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2a67e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a67e-133">NOTES</span></span>

## <span data-ttu-id="2a67e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a67e-134">RELATED LINKS</span></span>

[<span data-ttu-id="2a67e-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a67e-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2a67e-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="2a67e-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="2a67e-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a67e-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2a67e-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a67e-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="2a67e-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2a67e-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

