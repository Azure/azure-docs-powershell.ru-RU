---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243374"
---
# <span data-ttu-id="73015-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="73015-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="73015-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73015-102">SYNOPSIS</span></span>
<span data-ttu-id="73015-103">Получение указанного выходных данных запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="73015-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="73015-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73015-104">SYNTAX</span></span>

### <span data-ttu-id="73015-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73015-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73015-106">Получить</span><span class="sxs-lookup"><span data-stu-id="73015-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73015-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73015-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="73015-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73015-108">DESCRIPTION</span></span>
<span data-ttu-id="73015-109">Получение указанного выходных данных запуска для указанного ресурса шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="73015-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="73015-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73015-110">EXAMPLES</span></span>

### <span data-ttu-id="73015-111">Пример 1: список всех результатов выполнения в шаблоне</span><span class="sxs-lookup"><span data-stu-id="73015-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="73015-112">Эта команда выводит список всех результатов выполнения в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="73015-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="73015-113">Пример 2: получение результата выполнения в шаблоне</span><span class="sxs-lookup"><span data-stu-id="73015-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="73015-114">Эта команда получает результат выполнения в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="73015-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="73015-115">Пример 3: получение результата выполнения в шаблоне</span><span class="sxs-lookup"><span data-stu-id="73015-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="73015-116">Эта команда получает результат выполнения в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="73015-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="73015-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73015-117">PARAMETERS</span></span>

### <span data-ttu-id="73015-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73015-118">-DefaultProfile</span></span>
<span data-ttu-id="73015-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73015-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73015-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="73015-120">-ImageTemplateName</span></span>
<span data-ttu-id="73015-121">Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="73015-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73015-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73015-122">-InputObject</span></span>
<span data-ttu-id="73015-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="73015-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73015-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73015-124">-ResourceGroupName</span></span>
<span data-ttu-id="73015-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73015-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73015-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="73015-126">-RunOutputName</span></span>
<span data-ttu-id="73015-127">Имя выходных данных запуска</span><span class="sxs-lookup"><span data-stu-id="73015-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73015-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73015-128">-SubscriptionId</span></span>
<span data-ttu-id="73015-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73015-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="73015-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="73015-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73015-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73015-131">CommonParameters</span></span>
<span data-ttu-id="73015-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73015-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73015-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73015-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73015-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73015-134">INPUTS</span></span>

### <span data-ttu-id="73015-135">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="73015-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="73015-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73015-136">OUTPUTS</span></span>

### <span data-ttu-id="73015-137">Microsoft. Azure. PowerShell. командлеты. ImageBuilder. Models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="73015-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="73015-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="73015-138">NOTES</span></span>

<span data-ttu-id="73015-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="73015-139">ALIASES</span></span>

<span data-ttu-id="73015-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="73015-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73015-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="73015-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73015-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73015-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73015-143">INPUTOBJECT <IImageBuilderIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="73015-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73015-144">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="73015-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73015-145">`[ImageTemplateName <String>]`: Имя шаблона изображения</span><span class="sxs-lookup"><span data-stu-id="73015-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="73015-146">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73015-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="73015-147">`[RunOutputName <String>]`: Имя выходных данных запуска</span><span class="sxs-lookup"><span data-stu-id="73015-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="73015-148">`[SubscriptionId <String>]`: Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73015-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="73015-149">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="73015-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="73015-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73015-150">RELATED LINKS</span></span>

