---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566885"
---
# <span data-ttu-id="e9bda-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e9bda-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="e9bda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9bda-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bda-103">Отменяет асинхронную операцию обновления в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e9bda-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9bda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9bda-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9bda-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9bda-105">DESCRIPTION</span></span>
<span data-ttu-id="e9bda-106">Командлет **Stop-AzureRmSqlElasticPoolActivity** отменяет асинхронную операцию обновления в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e9bda-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="e9bda-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9bda-107">EXAMPLES</span></span>

### <span data-ttu-id="e9bda-108">Пример 1: Отмена асинхронной операции обновления для пула эластичных БД</span><span class="sxs-lookup"><span data-stu-id="e9bda-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
```

<span data-ttu-id="e9bda-109">Эта команда отменяет операцию асинхронных обновлений в пуле эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e9bda-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="e9bda-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9bda-110">PARAMETERS</span></span>

### <span data-ttu-id="e9bda-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bda-111">-DefaultProfile</span></span>
<span data-ttu-id="e9bda-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bda-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bda-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e9bda-113">-ElasticPoolName</span></span>
<span data-ttu-id="e9bda-114">Имя пула эластичных БД SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bda-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="e9bda-115">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="e9bda-115">-OperationId</span></span>
<span data-ttu-id="e9bda-116">ИДЕНТИФИКАТОР операции, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="e9bda-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9bda-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bda-117">-ResourceGroupName</span></span>
<span data-ttu-id="e9bda-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e9bda-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9bda-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e9bda-119">-ServerName</span></span>
<span data-ttu-id="e9bda-120">Имя сервера Azure SQL Server, в котором находится пул эластичных БД.</span><span class="sxs-lookup"><span data-stu-id="e9bda-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="e9bda-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9bda-121">-Confirm</span></span>
<span data-ttu-id="e9bda-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9bda-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bda-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9bda-123">-WhatIf</span></span>
<span data-ttu-id="e9bda-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9bda-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9bda-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9bda-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bda-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bda-126">CommonParameters</span></span>
<span data-ttu-id="e9bda-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9bda-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bda-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9bda-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bda-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9bda-129">INPUTS</span></span>

### <span data-ttu-id="e9bda-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="e9bda-130">None</span></span>

<span data-ttu-id="e9bda-131">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="e9bda-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e9bda-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9bda-132">OUTPUTS</span></span>

### <span data-ttu-id="e9bda-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="e9bda-133">System.Object</span></span>

## <span data-ttu-id="e9bda-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9bda-134">NOTES</span></span>

## <span data-ttu-id="e9bda-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9bda-135">RELATED LINKS</span></span>



