---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: b58ec1f76737f34664bdecef38f2b596be3702d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728845"
---
# <span data-ttu-id="a7a41-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7a41-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="a7a41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7a41-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a41-103">Удаляет пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="a7a41-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="a7a41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7a41-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7a41-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a41-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a41-106">Командлет **Remove-AzSqlElasticPool** удаляет пул эластичных БД базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a41-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="a7a41-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7a41-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a41-108">Пример 1: удаление эластичного пула</span><span class="sxs-lookup"><span data-stu-id="a7a41-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a7a41-109">Эта команда удаляет эластичный пул с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a7a41-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="a7a41-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7a41-110">PARAMETERS</span></span>

### <span data-ttu-id="a7a41-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a41-111">-DefaultProfile</span></span>
<span data-ttu-id="a7a41-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a7a41-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7a41-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a7a41-113">-ElasticPoolName</span></span>
<span data-ttu-id="a7a41-114">Указывает имя эластичного пула, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a7a41-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="a7a41-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a7a41-115">-Force</span></span>
<span data-ttu-id="a7a41-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a7a41-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7a41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a41-117">-ResourceGroupName</span></span>
<span data-ttu-id="a7a41-118">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="a7a41-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="a7a41-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a7a41-119">-ServerName</span></span>
<span data-ttu-id="a7a41-120">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="a7a41-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="a7a41-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7a41-121">-Confirm</span></span>
<span data-ttu-id="a7a41-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a7a41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a41-123">-WhatIf</span></span>
<span data-ttu-id="a7a41-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a7a41-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a41-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a7a41-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a41-126">CommonParameters</span></span>
<span data-ttu-id="a7a41-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7a41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a41-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7a41-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a41-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7a41-129">INPUTS</span></span>

### <span data-ttu-id="a7a41-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a41-130">System.String</span></span>

## <span data-ttu-id="a7a41-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a41-131">OUTPUTS</span></span>

### <span data-ttu-id="a7a41-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="a7a41-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a7a41-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7a41-133">NOTES</span></span>

## <span data-ttu-id="a7a41-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7a41-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7a41-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7a41-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="a7a41-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a7a41-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="a7a41-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a7a41-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="a7a41-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7a41-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="a7a41-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a7a41-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="a7a41-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a7a41-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


