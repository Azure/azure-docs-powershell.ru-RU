---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076352"
---
# <span data-ttu-id="99930-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99930-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="99930-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99930-102">SYNOPSIS</span></span>
<span data-ttu-id="99930-103">Возвращает среды Azure</span><span class="sxs-lookup"><span data-stu-id="99930-103">Gets Azure environments</span></span>

## <span data-ttu-id="99930-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99930-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99930-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99930-105">DESCRIPTION</span></span>
<span data-ttu-id="99930-106">Командлет **Get-AzureEnvironment** получает среды Azure, доступные для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99930-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="99930-107">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="99930-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="99930-108">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="99930-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="99930-109">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="99930-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="99930-110">Командлет **Get-AzureEnvironment** получает среды из файла данных подписки, а не из Azure.</span><span class="sxs-lookup"><span data-stu-id="99930-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="99930-111">Если файл данных подписки устарел, выполните командлет **Add-AzureAccount** или **Import-PublishSettingsFile** , чтобы обновить его.</span><span class="sxs-lookup"><span data-stu-id="99930-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="99930-112">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99930-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="99930-113">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="99930-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="99930-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99930-114">EXAMPLES</span></span>

### <span data-ttu-id="99930-115">Пример 1: получение всех сред</span><span class="sxs-lookup"><span data-stu-id="99930-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="99930-116">Эта команда получает все среды, доступные для Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="99930-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="99930-117">Пример 2: получение среды по имени</span><span class="sxs-lookup"><span data-stu-id="99930-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="99930-118">Этот пример возвращает среду AzureCloud.</span><span class="sxs-lookup"><span data-stu-id="99930-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="99930-119">Пример 3: получение всех свойств всех сред</span><span class="sxs-lookup"><span data-stu-id="99930-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="99930-120">Эта команда получает все свойства всех сред.</span><span class="sxs-lookup"><span data-stu-id="99930-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="99930-121">В команде используется командлет **Get-AzureEnvironment** , чтобы получить все среды Azure для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="99930-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="99930-122">Затем он использует командлет **ForEach-Object** для выполнения команды **Get-AzureEnvironment** с параметром **Name** в каждой среде.</span><span class="sxs-lookup"><span data-stu-id="99930-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="99930-123">Значением параметра **Name** является свойство **EnvironmentName** каждой среды.</span><span class="sxs-lookup"><span data-stu-id="99930-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="99930-124">Без параметров **Get-AzureEnvironment** возвращает только выбранные свойства среды.</span><span class="sxs-lookup"><span data-stu-id="99930-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="99930-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99930-125">PARAMETERS</span></span>

### <span data-ttu-id="99930-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99930-126">-Name</span></span>
<span data-ttu-id="99930-127">Получает только указанную среду.</span><span class="sxs-lookup"><span data-stu-id="99930-127">Gets only the specified environment.</span></span>
<span data-ttu-id="99930-128">Введите имя среды.</span><span class="sxs-lookup"><span data-stu-id="99930-128">Type the environment name.</span></span>
<span data-ttu-id="99930-129">Значение параметра задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="99930-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="99930-130">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="99930-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99930-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="99930-131">-Profile</span></span>
<span data-ttu-id="99930-132">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="99930-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="99930-133">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="99930-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99930-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99930-134">CommonParameters</span></span>
<span data-ttu-id="99930-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99930-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99930-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99930-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99930-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99930-137">INPUTS</span></span>

### <span data-ttu-id="99930-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="99930-138">None</span></span>
<span data-ttu-id="99930-139">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="99930-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="99930-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99930-140">OUTPUTS</span></span>

### <span data-ttu-id="99930-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="99930-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="99930-142">По умолчанию **Get-AzureEnvironment** Возвращает настраиваемый объект.</span><span class="sxs-lookup"><span data-stu-id="99930-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="99930-143">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99930-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="99930-144">При запуске **Get-AzureEnvironment** с параметром **Name** возвращается объект  **WindowsAzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="99930-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="99930-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="99930-145">NOTES</span></span>

## <span data-ttu-id="99930-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99930-146">RELATED LINKS</span></span>

[<span data-ttu-id="99930-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="99930-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="99930-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99930-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="99930-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="99930-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="99930-150">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="99930-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="99930-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99930-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="99930-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99930-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


