---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075967"
---
# <span data-ttu-id="7bc87-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7bc87-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="7bc87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bc87-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc87-103">Изменяет свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc87-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="7bc87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bc87-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7bc87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bc87-105">DESCRIPTION</span></span>
<span data-ttu-id="7bc87-106">Командлет **Set-AzureEnvironment** изменяет свойства среды Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc87-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="7bc87-107">Функция возвращает объект, который представляет среду с новыми значениями свойств.</span><span class="sxs-lookup"><span data-stu-id="7bc87-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="7bc87-108">Используйте параметр **Name** для идентификации среды и других параметров для изменения значений свойств.</span><span class="sxs-lookup"><span data-stu-id="7bc87-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="7bc87-109">Нельзя использовать **Set-AzureEnvironment** , чтобы изменить имя среды Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc87-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="7bc87-110">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="7bc87-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="7bc87-111">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="7bc87-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="7bc87-112">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7bc87-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="7bc87-113">Примечание. не изменяйте свойства сред AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7bc87-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="7bc87-114">Используйте этот командлет для изменения значений частных сред, которые вы создаете.</span><span class="sxs-lookup"><span data-stu-id="7bc87-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="7bc87-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bc87-115">EXAMPLES</span></span>

### <span data-ttu-id="7bc87-116">Пример 1: изменение свойств среды</span><span class="sxs-lookup"><span data-stu-id="7bc87-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="7bc87-117">Эта команда изменяет значения свойств **PublishSettingsFileUrl** и **StorageEndpoint** среды ContosoEnv.</span><span class="sxs-lookup"><span data-stu-id="7bc87-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="7bc87-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bc87-118">PARAMETERS</span></span>

### <span data-ttu-id="7bc87-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="7bc87-120">Изменяет указанное значение конечной точки для проверки подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7bc87-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc87-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="7bc87-122">Указывает идентификатор API управления, доступ к которому управляется службой Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7bc87-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="7bc87-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="7bc87-123">-AdTenant</span></span>
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

### <span data-ttu-id="7bc87-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7bc87-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="7bc87-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc87-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="7bc87-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="7bc87-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-127">-GalleryEndpoint</span></span>
<span data-ttu-id="7bc87-128">Изменяет конечную точку для коллекции диспетчера ресурсов Azure указанным значением.</span><span class="sxs-lookup"><span data-stu-id="7bc87-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="7bc87-129">Конечная точка галереи — это расположение шаблонов коллекции групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bc87-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="7bc87-130">Дополнительные сведения о группах ресурсов Azure и шаблонах коллекций можно найти в разделе справки по запросу [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span><span class="sxs-lookup"><span data-stu-id="7bc87-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="7bc87-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="7bc87-133">Изменение URL-адреса портала управления Azure на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="7bc87-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="7bc87-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bc87-134">-Name</span></span>
<span data-ttu-id="7bc87-135">Определяет среду, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7bc87-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="7bc87-136">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="7bc87-136">This parameter is required.</span></span>
<span data-ttu-id="7bc87-137">Значение параметра задается с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="7bc87-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="7bc87-138">Подстановочные знаки не разрешены.</span><span class="sxs-lookup"><span data-stu-id="7bc87-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="7bc87-139">-Profile</span></span>
<span data-ttu-id="7bc87-140">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7bc87-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7bc87-141">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bc87-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7bc87-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="7bc87-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="7bc87-143">Изменяет URL-адрес для файлов параметров публикации в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="7bc87-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="7bc87-144">Файл параметров публикации Azure — это XML-файл, который содержит сведения о вашей учетной записи и сертификате управления, позволяющий Windows PowerShell войти в свою учетную запись Azure от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="7bc87-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="7bc87-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="7bc87-146">Изменяет конечную точку для данных диспетчера ресурсов Azure, включая данные о группах ресурсов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="7bc87-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="7bc87-147">Дополнительные сведения об диспетчере ресурсов Azure можно найти в [командлетах диспетчера ресурсов Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) и [с помощью Windows PowerShell с диспетчером ресурсов](https://go.microsoft.com/fwlink/?LinkID=394767)  ) ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="7bc87-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-148">-ServiceEndpoint</span></span>
<span data-ttu-id="7bc87-149">Изменяет URL-адрес конечной точки службы Azure в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="7bc87-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="7bc87-150">Конечная точка службы Azure определяет, управляет ли ваше приложение глобальной платформой Azure, службой Azure, предоставляемой 21Vianet в Китае, или частным экземпляром Azure.</span><span class="sxs-lookup"><span data-stu-id="7bc87-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7bc87-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="7bc87-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="7bc87-152">-StorageEndpoint</span></span>
<span data-ttu-id="7bc87-153">Изменяет конечную точку по умолчанию служб хранилища в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="7bc87-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc87-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="7bc87-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="7bc87-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc87-155">CommonParameters</span></span>
<span data-ttu-id="7bc87-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bc87-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc87-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc87-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc87-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bc87-158">INPUTS</span></span>

### <span data-ttu-id="7bc87-159">Ничего</span><span class="sxs-lookup"><span data-stu-id="7bc87-159">None</span></span>
<span data-ttu-id="7bc87-160">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="7bc87-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7bc87-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bc87-161">OUTPUTS</span></span>

### <span data-ttu-id="7bc87-162">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7bc87-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="7bc87-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bc87-163">NOTES</span></span>

## <span data-ttu-id="7bc87-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bc87-164">RELATED LINKS</span></span>

[<span data-ttu-id="7bc87-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7bc87-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="7bc87-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7bc87-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="7bc87-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7bc87-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


