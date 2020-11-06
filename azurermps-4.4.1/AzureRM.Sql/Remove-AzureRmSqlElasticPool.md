---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566271"
---
# <span data-ttu-id="89621-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89621-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="89621-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89621-102">SYNOPSIS</span></span>
<span data-ttu-id="89621-103">Удаляет пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="89621-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89621-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89621-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89621-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89621-105">DESCRIPTION</span></span>
<span data-ttu-id="89621-106">Командлет **Remove-AzureRmSqlElasticPool** удаляет пул эластичных БД базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="89621-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="89621-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89621-107">EXAMPLES</span></span>

### <span data-ttu-id="89621-108">Пример 1: удаление эластичного пула</span><span class="sxs-lookup"><span data-stu-id="89621-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="89621-109">Эта команда удаляет эластичный пул с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="89621-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="89621-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89621-110">PARAMETERS</span></span>

### <span data-ttu-id="89621-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="89621-111">-ElasticPoolName</span></span>
<span data-ttu-id="89621-112">Указывает имя эластичного пула, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="89621-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="89621-113">-Force</span><span class="sxs-lookup"><span data-stu-id="89621-113">-Force</span></span>
<span data-ttu-id="89621-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="89621-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89621-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89621-115">-ResourceGroupName</span></span>
<span data-ttu-id="89621-116">Указывает имя группы ресурсов, которой назначен эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="89621-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="89621-117">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="89621-117">-ServerName</span></span>
<span data-ttu-id="89621-118">Указывает имя сервера, на котором размещается эластичный пул.</span><span class="sxs-lookup"><span data-stu-id="89621-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="89621-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89621-119">-Confirm</span></span>
<span data-ttu-id="89621-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89621-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89621-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89621-121">-WhatIf</span></span>
<span data-ttu-id="89621-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89621-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89621-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89621-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89621-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89621-124">-DefaultProfile</span></span>
<span data-ttu-id="89621-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89621-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89621-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89621-126">CommonParameters</span></span>
<span data-ttu-id="89621-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89621-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89621-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89621-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89621-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89621-129">INPUTS</span></span>

### <span data-ttu-id="89621-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="89621-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="89621-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89621-131">OUTPUTS</span></span>

### <span data-ttu-id="89621-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="89621-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="89621-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="89621-133">NOTES</span></span>

## <span data-ttu-id="89621-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89621-134">RELATED LINKS</span></span>

[<span data-ttu-id="89621-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89621-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="89621-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="89621-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="89621-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="89621-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="89621-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89621-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="89621-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="89621-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="89621-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="89621-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


