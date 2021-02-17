---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243413"
---
# <span data-ttu-id="c9527-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="c9527-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="c9527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9527-102">SYNOPSIS</span></span>
<span data-ttu-id="c9527-103">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="c9527-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="c9527-104">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="c9527-104">A location is an Azure region.</span></span>

## <span data-ttu-id="c9527-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9527-105">SYNTAX</span></span>

### <span data-ttu-id="c9527-106">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c9527-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c9527-107">Получить</span><span class="sxs-lookup"><span data-stu-id="c9527-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c9527-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c9527-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9527-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9527-109">DESCRIPTION</span></span>
<span data-ttu-id="c9527-110">Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.</span><span class="sxs-lookup"><span data-stu-id="c9527-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="c9527-111">Расположение — это регион Azure.</span><span class="sxs-lookup"><span data-stu-id="c9527-111">A location is an Azure region.</span></span>

## <span data-ttu-id="c9527-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9527-112">EXAMPLES</span></span>

### <span data-ttu-id="c9527-113">Пример 1. Получите все сведения о расположении региона Azure с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9527-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="c9527-114">Этот cmdlet получает все сведения о расположении региона Azure с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c9527-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="c9527-115">Пример 2. Просмотр сведений о расположении региона Azure по имени расположения</span><span class="sxs-lookup"><span data-stu-id="c9527-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="c9527-116">Этот cmdlet получает сведения о расположении региона Azure по имени расположения.</span><span class="sxs-lookup"><span data-stu-id="c9527-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="c9527-117">Пример 3. Просмотр сведений о расположении региона Azure по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="c9527-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="c9527-118">Эти списки с помощью этих списков можно скомкалить сведения о расположении региона Azure по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="c9527-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="c9527-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9527-119">PARAMETERS</span></span>

### <span data-ttu-id="c9527-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c9527-120">-AcceptLanguage</span></span>
<span data-ttu-id="c9527-121">Указывает предпочтительный язык для ответа.</span><span class="sxs-lookup"><span data-stu-id="c9527-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="c9527-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9527-122">-DefaultProfile</span></span>
<span data-ttu-id="c9527-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9527-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9527-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9527-124">-InputObject</span></span>
<span data-ttu-id="c9527-125">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c9527-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c9527-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c9527-126">-Name</span></span>
<span data-ttu-id="c9527-127">Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="c9527-127">The name of the location.</span></span>
<span data-ttu-id="c9527-128">Например, "Запад США" или "запад".</span><span class="sxs-lookup"><span data-stu-id="c9527-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="c9527-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9527-129">CommonParameters</span></span>
<span data-ttu-id="c9527-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9527-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9527-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9527-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9527-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9527-132">INPUTS</span></span>

### <span data-ttu-id="c9527-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="c9527-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="c9527-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9527-134">OUTPUTS</span></span>

### <span data-ttu-id="c9527-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="c9527-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="c9527-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9527-136">NOTES</span></span>

<span data-ttu-id="c9527-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c9527-137">ALIASES</span></span>

<span data-ttu-id="c9527-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c9527-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c9527-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c9527-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c9527-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c9527-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c9527-141">INPUTOBJECT <IImportExportIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c9527-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c9527-142">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c9527-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c9527-143">`[JobName <String>]`: имя задания импорта и экспорта.</span><span class="sxs-lookup"><span data-stu-id="c9527-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="c9527-144">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="c9527-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="c9527-145">Например, "Запад США" или "запад".</span><span class="sxs-lookup"><span data-stu-id="c9527-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="c9527-146">`[ResourceGroupName <String>]`. Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.</span><span class="sxs-lookup"><span data-stu-id="c9527-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="c9527-147">`[SubscriptionId <String>]`: ИД подписки для пользователя Azure.</span><span class="sxs-lookup"><span data-stu-id="c9527-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="c9527-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9527-148">RELATED LINKS</span></span>

