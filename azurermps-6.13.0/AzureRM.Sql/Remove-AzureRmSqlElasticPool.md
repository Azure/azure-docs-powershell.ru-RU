---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3786dc0a9500dd07b332dacfbb026b5a44f0b550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733790"
---
# <span data-ttu-id="8f354-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8f354-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="8f354-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f354-102">SYNOPSIS</span></span>
<span data-ttu-id="8f354-103">Удаляет пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="8f354-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f354-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f354-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f354-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f354-105">DESCRIPTION</span></span>
<span data-ttu-id="8f354-106">Командлет **Remove-AzureRmSqlElasticPool** удаляет пул эластичных БД базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8f354-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="8f354-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f354-107">EXAMPLES</span></span>

### <span data-ttu-id="8f354-108">Пример 1: удаление эластичного пула</span><span class="sxs-lookup"><span data-stu-id="8f354-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="8f354-109">Эта команда удаляет эластичный пул с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="8f354-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="8f354-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f354-110">PARAMETERS</span></span>

### <span data-ttu-id="8f354-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f354-111">-DefaultProfile</span></span>
<span data-ttu-id="8f354-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f354-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f354-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8f354-113">-ElasticPoolName</span></span>
<span data-ttu-id="8f354-114">Указывает имя эластичного пула, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8f354-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8f354-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f354-115">-Force</span></span>
<span data-ttu-id="8f354-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f354-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f354-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f354-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f354-118">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="8f354-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="8f354-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8f354-119">-ServerName</span></span>
<span data-ttu-id="8f354-120">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="8f354-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="8f354-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f354-121">-Confirm</span></span>
<span data-ttu-id="8f354-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f354-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f354-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f354-123">-WhatIf</span></span>
<span data-ttu-id="8f354-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f354-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f354-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f354-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f354-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f354-126">CommonParameters</span></span>
<span data-ttu-id="8f354-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f354-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f354-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f354-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f354-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f354-129">INPUTS</span></span>

### <span data-ttu-id="8f354-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8f354-130">System.String</span></span>

## <span data-ttu-id="8f354-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f354-131">OUTPUTS</span></span>

### <span data-ttu-id="8f354-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="8f354-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="8f354-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f354-133">NOTES</span></span>

## <span data-ttu-id="8f354-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f354-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f354-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8f354-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8f354-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8f354-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="8f354-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8f354-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="8f354-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8f354-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8f354-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8f354-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8f354-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="8f354-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


