---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066642"
---
# <span data-ttu-id="c389e-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c389e-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="c389e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c389e-102">SYNOPSIS</span></span>
<span data-ttu-id="c389e-103">Получение сведений о заданиях Databox</span><span class="sxs-lookup"><span data-stu-id="c389e-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="c389e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c389e-104">SYNTAX</span></span>

### <span data-ttu-id="c389e-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c389e-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c389e-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c389e-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c389e-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c389e-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c389e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c389e-108">DESCRIPTION</span></span>
<span data-ttu-id="c389e-109">Командлет **Get-AzDataBoxJobs** получает сведения о заданиях databox в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="c389e-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="c389e-110">Если указана группа ресурсов, этот командлет получает все задания databox в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c389e-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="c389e-111">Если указать имя задания вместе с именем группы ресурсов, этот командлет получает сведения об этом конкретном задании databox.</span><span class="sxs-lookup"><span data-stu-id="c389e-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="c389e-112">Если не указать ничего, кроме идентификатора подписки, этот командлет получает сведения обо всех заданиях databox в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="c389e-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="c389e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c389e-113">EXAMPLES</span></span>

### <span data-ttu-id="c389e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c389e-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="c389e-115">Get-AzDataBoxJob без параметров выборка всех заданий databox в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="c389e-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="c389e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c389e-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="c389e-117">Get-AzDataBoxJob с параметром ResourceGroupName извлекает все задания databox в рамках указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c389e-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="c389e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c389e-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c389e-119">Get-AzDataBoxJob с ResourceGroupName и указанным именем будут получать данное задание databox</span><span class="sxs-lookup"><span data-stu-id="c389e-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="c389e-120">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c389e-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c389e-121">Get-AzDataBoxJob с указанием ResourceId извлекает это конкретное задание databox</span><span class="sxs-lookup"><span data-stu-id="c389e-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="c389e-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c389e-122">PARAMETERS</span></span>

### <span data-ttu-id="c389e-123">-Прервано</span><span class="sxs-lookup"><span data-stu-id="c389e-123">-Aborted</span></span>
<span data-ttu-id="c389e-124">Параметр Switch для получения прерванных заданий</span><span class="sxs-lookup"><span data-stu-id="c389e-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-125">-Отменено</span><span class="sxs-lookup"><span data-stu-id="c389e-125">-Cancelled</span></span>
<span data-ttu-id="c389e-126">Переключить параметр для получения отмененных заданий</span><span class="sxs-lookup"><span data-stu-id="c389e-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-127">-Завершено</span><span class="sxs-lookup"><span data-stu-id="c389e-127">-Completed</span></span>
<span data-ttu-id="c389e-128">Переключение параметров для получения завершенных заданий</span><span class="sxs-lookup"><span data-stu-id="c389e-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="c389e-129">-CompletedWithError</span></span>
<span data-ttu-id="c389e-130">Параметр переключения на выборку заданий, выполненных с ошибками</span><span class="sxs-lookup"><span data-stu-id="c389e-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c389e-131">-DefaultProfile</span></span>
<span data-ttu-id="c389e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c389e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c389e-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c389e-133">-Name</span></span>
<span data-ttu-id="c389e-134">Название задания Databox</span><span class="sxs-lookup"><span data-stu-id="c389e-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c389e-135">-ResourceGroupName</span></span>
<span data-ttu-id="c389e-136">Имя группы ресурсов "работа Databox"</span><span class="sxs-lookup"><span data-stu-id="c389e-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c389e-137">-ResourceId</span></span>
<span data-ttu-id="c389e-138">Код ресурса задания Databox</span><span class="sxs-lookup"><span data-stu-id="c389e-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c389e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c389e-139">CommonParameters</span></span>
<span data-ttu-id="c389e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c389e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c389e-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c389e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c389e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c389e-142">INPUTS</span></span>

### <span data-ttu-id="c389e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c389e-143">System.String</span></span>

## <span data-ttu-id="c389e-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c389e-144">OUTPUTS</span></span>

### <span data-ttu-id="c389e-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c389e-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="c389e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c389e-146">NOTES</span></span>

## <span data-ttu-id="c389e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c389e-147">RELATED LINKS</span></span>
