---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732397"
---
# <span data-ttu-id="7777e-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="7777e-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="7777e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7777e-102">SYNOPSIS</span></span>
<span data-ttu-id="7777e-103">Возвращает состояние операций в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="7777e-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7777e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7777e-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7777e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7777e-105">DESCRIPTION</span></span>
<span data-ttu-id="7777e-106">Командлет **Get-AzureRmSqlElasticPoolActivity** получает состояние операций в пуле эластичных БД для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7777e-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="7777e-107">Вы можете наблюдать за состоянием создания пулов и обновлений конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7777e-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="7777e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7777e-108">EXAMPLES</span></span>

### <span data-ttu-id="7777e-109">Пример 1: получение состояния операций для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="7777e-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="7777e-110">Эта команда возвращает состояние операций для пула эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="7777e-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="7777e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7777e-111">PARAMETERS</span></span>

### <span data-ttu-id="7777e-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7777e-112">-ElasticPoolName</span></span>
<span data-ttu-id="7777e-113">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="7777e-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="7777e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7777e-114">-ResourceGroupName</span></span>
<span data-ttu-id="7777e-115">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="7777e-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="7777e-116">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7777e-116">-ServerName</span></span>
<span data-ttu-id="7777e-117">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="7777e-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="7777e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7777e-118">-Confirm</span></span>
<span data-ttu-id="7777e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7777e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7777e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7777e-120">-WhatIf</span></span>
<span data-ttu-id="7777e-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7777e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7777e-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7777e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7777e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7777e-123">-DefaultProfile</span></span>
<span data-ttu-id="7777e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7777e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7777e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7777e-125">CommonParameters</span></span>
<span data-ttu-id="7777e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7777e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7777e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7777e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7777e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7777e-128">INPUTS</span></span>

## <span data-ttu-id="7777e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7777e-129">OUTPUTS</span></span>

### <span data-ttu-id="7777e-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="7777e-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="7777e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7777e-131">NOTES</span></span>

## <span data-ttu-id="7777e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7777e-132">RELATED LINKS</span></span>

[<span data-ttu-id="7777e-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7777e-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7777e-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="7777e-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="7777e-135">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7777e-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7777e-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7777e-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="7777e-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7777e-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


