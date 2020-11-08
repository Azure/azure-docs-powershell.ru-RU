---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076744"
---
# <span data-ttu-id="3b8f2-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="3b8f2-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="3b8f2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8f2-103">Возвращает конкретный образ платформы, соответствующий издателю, предложению SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="3b8f2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b8f2-104">SYNTAX</span></span>

### <span data-ttu-id="3b8f2-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b8f2-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8f2-106">Получить</span><span class="sxs-lookup"><span data-stu-id="3b8f2-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3b8f2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3b8f2-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3b8f2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b8f2-108">DESCRIPTION</span></span>
<span data-ttu-id="3b8f2-109">Возвращает конкретный образ платформы, соответствующий издателю, предложению SKU и версии.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="3b8f2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b8f2-110">EXAMPLES</span></span>

### <span data-ttu-id="3b8f2-111">Пример 1: получение всех образов платформы</span><span class="sxs-lookup"><span data-stu-id="3b8f2-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="3b8f2-112">Получите список всех образов платформы, оставив все параметры пустыми.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="3b8f2-113">Пример 2: получение определенного образа платформы</span><span class="sxs-lookup"><span data-stu-id="3b8f2-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="3b8f2-114">Укажите предложение, издатель, расположение, SKU и версию, чтобы получить изображение платформы.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="3b8f2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b8f2-115">PARAMETERS</span></span>

### <span data-ttu-id="3b8f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8f2-116">-DefaultProfile</span></span>
<span data-ttu-id="3b8f2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b8f2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b8f2-118">-InputObject</span></span>
<span data-ttu-id="3b8f2-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3b8f2-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3b8f2-120">-Location</span></span>
<span data-ttu-id="3b8f2-121">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b8f2-122">-Предложение</span><span class="sxs-lookup"><span data-stu-id="3b8f2-122">-Offer</span></span>
<span data-ttu-id="3b8f2-123">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-123">Name of the offer.</span></span>

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

### <span data-ttu-id="3b8f2-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3b8f2-124">-Publisher</span></span>
<span data-ttu-id="3b8f2-125">Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="3b8f2-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="3b8f2-126">-Sku</span></span>
<span data-ttu-id="3b8f2-127">Название SKU.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="3b8f2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b8f2-128">-SubscriptionId</span></span>
<span data-ttu-id="3b8f2-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b8f2-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3b8f2-131">-Version</span><span class="sxs-lookup"><span data-stu-id="3b8f2-131">-Version</span></span>
<span data-ttu-id="3b8f2-132">Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-132">The version of the resource.</span></span>

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

### <span data-ttu-id="3b8f2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8f2-133">CommonParameters</span></span>
<span data-ttu-id="3b8f2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8f2-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b8f2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8f2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b8f2-136">INPUTS</span></span>

### <span data-ttu-id="3b8f2-137">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3b8f2-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3b8f2-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b8f2-138">OUTPUTS</span></span>

### <span data-ttu-id="3b8f2-139">Microsoft. Azure. PowerShell. командлеты. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="3b8f2-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="3b8f2-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b8f2-140">NOTES</span></span>

<span data-ttu-id="3b8f2-141">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b8f2-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3b8f2-143">INPUTOBJECT <IComputeAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3b8f2-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b8f2-144">`[DiskId <String>]`: Идентификатор GUID диска.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3b8f2-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3b8f2-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b8f2-146">`[Location <String>]`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3b8f2-147">`[MigrationId <String>]`: Имя GUID задания миграции.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3b8f2-148">`[Offer <String>]`: Название предложения.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3b8f2-149">`[Publisher <String>]`: Имя издателя.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3b8f2-150">`[QuotaName <String>]`: Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3b8f2-151">`[Sku <String>]`: Имя SKU.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3b8f2-152">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3b8f2-153">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3b8f2-154">`[Type <String>]`: Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3b8f2-155">`[Version <String>]`: Версия ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b8f2-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3b8f2-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b8f2-156">RELATED LINKS</span></span>

