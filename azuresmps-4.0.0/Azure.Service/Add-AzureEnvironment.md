---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075730"
---
# <span data-ttu-id="d003a-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d003a-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="d003a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d003a-102">SYNOPSIS</span></span>
<span data-ttu-id="d003a-103">Создает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="d003a-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="d003a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d003a-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d003a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d003a-105">DESCRIPTION</span></span>
<span data-ttu-id="d003a-106">Командлет **Add-AzureEnvironment** создает новую пользовательскую среду учетной записи Azure и сохраняет ее в перемещаемом профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="d003a-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="d003a-107">Командлет возвращает объект, который представляет новую среду.</span><span class="sxs-lookup"><span data-stu-id="d003a-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="d003a-108">После завершения команды вы можете использовать среду в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d003a-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="d003a-109">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="d003a-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="d003a-110">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="d003a-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="d003a-111">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d003a-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="d003a-112">Только параметр **Name** этого командлета является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d003a-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="d003a-113">Если параметр не указан, его значение равно null ($Null), а служба, использующая конечную точку, может работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="d003a-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="d003a-114">Чтобы добавить или изменить значение свойства среды, используйте командлет **Set-AzureEnvironment** .</span><span class="sxs-lookup"><span data-stu-id="d003a-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="d003a-115">Примечание. изменение среды может привести к сбою вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d003a-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="d003a-116">Обычно среды добавляются только для тестирования и устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="d003a-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="d003a-117">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d003a-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d003a-118">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d003a-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d003a-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d003a-119">EXAMPLES</span></span>

### <span data-ttu-id="d003a-120">Пример 1: Добавление среды Azure</span><span class="sxs-lookup"><span data-stu-id="d003a-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="d003a-121">Эта команда создает среду ContosoEnv Azure.</span><span class="sxs-lookup"><span data-stu-id="d003a-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="d003a-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d003a-122">PARAMETERS</span></span>

### <span data-ttu-id="d003a-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="d003a-124">Задает конечную точку для проверки подлинности Azure Active Directory в новой среде.</span><span class="sxs-lookup"><span data-stu-id="d003a-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="d003a-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d003a-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="d003a-126">Указывает идентификатор API управления, доступ к которому управляется службой Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d003a-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="d003a-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="d003a-127">-AdTenant</span></span>
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

### <span data-ttu-id="d003a-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d003a-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="d003a-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d003a-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="d003a-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="d003a-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="d003a-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-131">-GalleryEndpoint</span></span>
<span data-ttu-id="d003a-132">Задает конечную точку для коллекции диспетчера ресурсов Azure, в которой хранятся шаблоны коллекции групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d003a-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="d003a-133">Дополнительные сведения о группах ресурсов Azure и шаблонах коллекций можно найти в разделе справки по запросу Get-AzureResourceGroupGalleryTemplate https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="d003a-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="d003a-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="d003a-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="d003a-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="d003a-136">Указывает URL-адрес портала управления Azure в новой среде.</span><span class="sxs-lookup"><span data-stu-id="d003a-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="d003a-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d003a-137">-Name</span></span>
<span data-ttu-id="d003a-138">Задает имя среды.</span><span class="sxs-lookup"><span data-stu-id="d003a-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="d003a-139">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d003a-139">This parameter is required.</span></span>
<span data-ttu-id="d003a-140">Не используйте имена сред по умолчанию, AzureCloud и AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="d003a-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="d003a-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="d003a-141">-Profile</span></span>
<span data-ttu-id="d003a-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d003a-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d003a-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d003a-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d003a-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="d003a-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="d003a-145">Задает URL-адрес файлов параметров публикации для вашей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="d003a-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="d003a-146">Файл параметров публикации Azure — это XML-файл, который содержит сведения о вашей учетной записи и сертификате управления, позволяющий Windows PowerShell войти в свою учетную запись Azure от вашего имени.</span><span class="sxs-lookup"><span data-stu-id="d003a-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="d003a-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="d003a-148">Задает конечную точку для данных диспетчера ресурсов Azure, включая данные о группах ресурсов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="d003a-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="d003a-149">Дополнительные сведения об диспетчере ресурсов Azure можно найти в [командлетах диспетчера ресурсов Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) и [с помощью Windows PowerShell с диспетчером ресурсов](https://go.microsoft.com/fwlink/?LinkID=394767)  ) ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="d003a-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="d003a-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-150">-ServiceEndpoint</span></span>
<span data-ttu-id="d003a-151">Указывает URL-адрес конечной точки службы Azure.</span><span class="sxs-lookup"><span data-stu-id="d003a-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="d003a-152">Конечная точка службы Azure определяет, управляет ли ваше приложение глобальной платформой Azure, службой Azure, предоставляемой 21Vianet в Китае, или частным экземпляром Azure.</span><span class="sxs-lookup"><span data-stu-id="d003a-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="d003a-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d003a-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="d003a-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="d003a-154">-StorageEndpoint</span></span>
<span data-ttu-id="d003a-155">Задает конечную точку по умолчанию служб хранилища в новой среде.</span><span class="sxs-lookup"><span data-stu-id="d003a-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="d003a-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d003a-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="d003a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d003a-157">CommonParameters</span></span>
<span data-ttu-id="d003a-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d003a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d003a-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d003a-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d003a-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d003a-160">INPUTS</span></span>

### <span data-ttu-id="d003a-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="d003a-161">None</span></span>
<span data-ttu-id="d003a-162">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="d003a-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d003a-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d003a-163">OUTPUTS</span></span>

### <span data-ttu-id="d003a-164">Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d003a-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="d003a-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="d003a-165">NOTES</span></span>

## <span data-ttu-id="d003a-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d003a-166">RELATED LINKS</span></span>

[<span data-ttu-id="d003a-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d003a-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="d003a-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d003a-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="d003a-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d003a-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


