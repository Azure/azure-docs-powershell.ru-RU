---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243906"
---
# <span data-ttu-id="9162e-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9162e-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="9162e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9162e-102">SYNOPSIS</span></span>
<span data-ttu-id="9162e-103">Удаляет пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="9162e-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="9162e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9162e-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9162e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9162e-105">DESCRIPTION</span></span>
<span data-ttu-id="9162e-106">Командлет **Remove-AzSqlElasticPool** удаляет пул эластичных БД базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9162e-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="9162e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9162e-107">EXAMPLES</span></span>

### <span data-ttu-id="9162e-108">Пример 1: удаление эластичного пула</span><span class="sxs-lookup"><span data-stu-id="9162e-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="9162e-109">Эта команда удаляет эластичный пул с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="9162e-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="9162e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9162e-110">PARAMETERS</span></span>

### <span data-ttu-id="9162e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9162e-111">-DefaultProfile</span></span>
<span data-ttu-id="9162e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9162e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9162e-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9162e-113">-ElasticPoolName</span></span>
<span data-ttu-id="9162e-114">Указывает имя эластичного пула, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9162e-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9162e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9162e-115">-Force</span></span>
<span data-ttu-id="9162e-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9162e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9162e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9162e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9162e-118">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="9162e-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="9162e-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9162e-119">-ServerName</span></span>
<span data-ttu-id="9162e-120">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="9162e-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="9162e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9162e-121">-Confirm</span></span>
<span data-ttu-id="9162e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9162e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9162e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9162e-123">-WhatIf</span></span>
<span data-ttu-id="9162e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9162e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9162e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9162e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9162e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9162e-126">CommonParameters</span></span>
<span data-ttu-id="9162e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9162e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9162e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9162e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9162e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9162e-129">INPUTS</span></span>

### <span data-ttu-id="9162e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9162e-130">System.String</span></span>

## <span data-ttu-id="9162e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9162e-131">OUTPUTS</span></span>

### <span data-ttu-id="9162e-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="9162e-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="9162e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9162e-133">NOTES</span></span>

## <span data-ttu-id="9162e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9162e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9162e-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9162e-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="9162e-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9162e-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="9162e-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="9162e-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="9162e-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9162e-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="9162e-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9162e-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="9162e-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="9162e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


