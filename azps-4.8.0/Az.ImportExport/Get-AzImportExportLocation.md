---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242749"
---
# <span data-ttu-id="5f255-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="5f255-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="5f255-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5f255-102">SYNOPSIS</span></span>
<span data-ttu-id="5f255-103">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="5f255-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="5f255-104">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="5f255-104">A location is an Azure region.</span></span>

## <span data-ttu-id="5f255-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5f255-105">SYNTAX</span></span>

### <span data-ttu-id="5f255-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f255-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f255-107">Получить</span><span class="sxs-lookup"><span data-stu-id="5f255-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f255-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5f255-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f255-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f255-109">DESCRIPTION</span></span>
<span data-ttu-id="5f255-110">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="5f255-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="5f255-111">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="5f255-111">A location is an Azure region.</span></span>

## <span data-ttu-id="5f255-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5f255-112">EXAMPLES</span></span>

### <span data-ttu-id="5f255-113">Пример 1: получение всех сведений о расположении областей Azure с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5f255-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="5f255-114">Этот командлет получает все сведения о расположении областей Azure с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5f255-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="5f255-115">Пример 2: получение сведений о расположении региона Azure по названию расположения</span><span class="sxs-lookup"><span data-stu-id="5f255-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="5f255-116">Этот командлет получает сведения о расположении региона Azure по названию расположения.</span><span class="sxs-lookup"><span data-stu-id="5f255-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="5f255-117">Пример 3: получение сведений о расположении региона Azure по удостоверению</span><span class="sxs-lookup"><span data-stu-id="5f255-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="5f255-118">Этот командлет возвращает сведения о расположении региона Azure по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="5f255-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="5f255-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5f255-119">PARAMETERS</span></span>

### <span data-ttu-id="5f255-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="5f255-120">-AcceptLanguage</span></span>
<span data-ttu-id="5f255-121">Указывает предпочтительный язык ответа.</span><span class="sxs-lookup"><span data-stu-id="5f255-121">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f255-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f255-122">-DefaultProfile</span></span>
<span data-ttu-id="5f255-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5f255-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f255-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f255-124">-InputObject</span></span>
<span data-ttu-id="5f255-125">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5f255-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f255-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5f255-126">-Name</span></span>
<span data-ttu-id="5f255-127">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="5f255-127">The name of the location.</span></span>
<span data-ttu-id="5f255-128">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="5f255-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f255-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f255-129">CommonParameters</span></span>
<span data-ttu-id="5f255-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5f255-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f255-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f255-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f255-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5f255-132">INPUTS</span></span>

### <span data-ttu-id="5f255-133">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="5f255-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="5f255-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f255-134">OUTPUTS</span></span>

### <span data-ttu-id="5f255-135">Microsoft. Azure. PowerShell. командлеты. ImportExport. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="5f255-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="5f255-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="5f255-136">NOTES</span></span>

<span data-ttu-id="5f255-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5f255-137">ALIASES</span></span>

<span data-ttu-id="5f255-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5f255-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f255-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5f255-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f255-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5f255-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f255-141">INPUTOBJECT <IImportExportIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="5f255-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f255-142">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="5f255-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f255-143">`[JobName <String>]`: Имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="5f255-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="5f255-144">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="5f255-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="5f255-145">Например, "Западная США" или "westus".</span><span class="sxs-lookup"><span data-stu-id="5f255-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="5f255-146">`[ResourceGroupName <String>]`: Имя группы ресурсов однозначно определяет группу ресурсов в пользовательской подписке.</span><span class="sxs-lookup"><span data-stu-id="5f255-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="5f255-147">`[SubscriptionId <String>]`: Идентификатор подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="5f255-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="5f255-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f255-148">RELATED LINKS</span></span>

