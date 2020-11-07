---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912936"
---
# <span data-ttu-id="512d3-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="512d3-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="512d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="512d3-102">SYNOPSIS</span></span>
<span data-ttu-id="512d3-103">Возвращает состояние операций в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="512d3-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="512d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="512d3-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="512d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="512d3-105">DESCRIPTION</span></span>
<span data-ttu-id="512d3-106">Командлет **Get-AzSqlElasticPoolActivity** получает состояние операций в пуле эластичных БД для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="512d3-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="512d3-107">Вы можете наблюдать за состоянием создания пулов и обновлений конфигурации.</span><span class="sxs-lookup"><span data-stu-id="512d3-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="512d3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="512d3-108">EXAMPLES</span></span>

### <span data-ttu-id="512d3-109">Пример 1: получение состояния операций для эластичного пула</span><span class="sxs-lookup"><span data-stu-id="512d3-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="512d3-110">Эта команда возвращает состояние операций для пула эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="512d3-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="512d3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="512d3-111">PARAMETERS</span></span>

### <span data-ttu-id="512d3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512d3-112">-DefaultProfile</span></span>
<span data-ttu-id="512d3-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="512d3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="512d3-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="512d3-114">-ElasticPoolName</span></span>
<span data-ttu-id="512d3-115">Указывает имя эластичного пула.</span><span class="sxs-lookup"><span data-stu-id="512d3-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="512d3-116">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="512d3-116">-OperationId</span></span>
<span data-ttu-id="512d3-117">ИДЕНТИФИКАТОР операции, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="512d3-117">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512d3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="512d3-118">-ResourceGroupName</span></span>
<span data-ttu-id="512d3-119">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="512d3-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="512d3-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="512d3-120">-ServerName</span></span>
<span data-ttu-id="512d3-121">Указывает имя сервера, который содержит эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="512d3-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="512d3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="512d3-122">-Confirm</span></span>
<span data-ttu-id="512d3-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="512d3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512d3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512d3-124">-WhatIf</span></span>
<span data-ttu-id="512d3-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="512d3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512d3-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="512d3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512d3-127">CommonParameters</span></span>
<span data-ttu-id="512d3-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="512d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512d3-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="512d3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512d3-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="512d3-130">INPUTS</span></span>

### <span data-ttu-id="512d3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="512d3-131">System.String</span></span>

### <span data-ttu-id="512d3-132">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="512d3-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="512d3-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="512d3-133">OUTPUTS</span></span>

### <span data-ttu-id="512d3-134">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="512d3-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="512d3-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="512d3-135">NOTES</span></span>

## <span data-ttu-id="512d3-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="512d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="512d3-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d3-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="512d3-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="512d3-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="512d3-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d3-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="512d3-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d3-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="512d3-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="512d3-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


