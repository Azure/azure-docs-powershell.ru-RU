---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 88052c9f47359e0080e193f5a2dbb1004b48b0e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732832"
---
# <span data-ttu-id="bc38a-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="bc38a-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="bc38a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc38a-102">SYNOPSIS</span></span>
<span data-ttu-id="bc38a-103">Возвращает состояние операций в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="bc38a-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc38a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc38a-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc38a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc38a-105">DESCRIPTION</span></span>
<span data-ttu-id="bc38a-106">Командлет **Get-AzureRmSqlElasticPoolActivity** получает состояние операций в пуле эластичных БД для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="bc38a-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="bc38a-107">Вы можете наблюдать за состоянием создания пулов и обновлений конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bc38a-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="bc38a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc38a-108">EXAMPLES</span></span>

### <span data-ttu-id="bc38a-109">Пример 1: получение состояния операций для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="bc38a-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="bc38a-110">Эта команда возвращает состояние операций для пула эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="bc38a-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="bc38a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc38a-111">PARAMETERS</span></span>

### <span data-ttu-id="bc38a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc38a-112">-DefaultProfile</span></span>
<span data-ttu-id="bc38a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bc38a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc38a-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="bc38a-114">-ElasticPoolName</span></span>
<span data-ttu-id="bc38a-115">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="bc38a-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="bc38a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc38a-116">-ResourceGroupName</span></span>
<span data-ttu-id="bc38a-117">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="bc38a-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="bc38a-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="bc38a-118">-ServerName</span></span>
<span data-ttu-id="bc38a-119">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="bc38a-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="bc38a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc38a-120">-Confirm</span></span>
<span data-ttu-id="bc38a-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc38a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc38a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc38a-122">-WhatIf</span></span>
<span data-ttu-id="bc38a-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc38a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc38a-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc38a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc38a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc38a-125">CommonParameters</span></span>
<span data-ttu-id="bc38a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc38a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc38a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc38a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc38a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc38a-128">INPUTS</span></span>

### <span data-ttu-id="bc38a-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc38a-129">None</span></span>
<span data-ttu-id="bc38a-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bc38a-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc38a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc38a-131">OUTPUTS</span></span>

### <span data-ttu-id="bc38a-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="bc38a-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="bc38a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc38a-133">NOTES</span></span>

## <span data-ttu-id="bc38a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc38a-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc38a-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc38a-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="bc38a-136">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="bc38a-136">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="bc38a-137">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc38a-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="bc38a-138">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc38a-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="bc38a-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="bc38a-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


