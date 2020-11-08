---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075883"
---
# <span data-ttu-id="6f2fb-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6f2fb-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="6f2fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f2fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2fb-103">Опубликуйте текущую службу в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="6f2fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f2fb-104">SYNTAX</span></span>

### <span data-ttu-id="6f2fb-105">PublishFromServiceDefinition (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f2fb-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6f2fb-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="6f2fb-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f2fb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2fb-107">DESCRIPTION</span></span>
<span data-ttu-id="6f2fb-108">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6f2fb-109">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6f2fb-110">Командлет **Publish-AzureServiceProject** публикует текущую службу в облаке.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="6f2fb-111">Вы можете указать конфигурацию публикации (например, **подписку** , **StorageAccountName** , **Расположение** , **гнездо** ) в командной строке или локальные параметры с помощью командлета **Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="6f2fb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f2fb-112">EXAMPLES</span></span>

### <span data-ttu-id="6f2fb-113">Пример 1: публикация проекта службы со значениями по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6f2fb-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="6f2fb-114">В этом примере текущая служба публикуется с использованием текущих параметров службы и текущего профиля публикации Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="6f2fb-115">Пример 2: создание пакета развертывания</span><span class="sxs-lookup"><span data-stu-id="6f2fb-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="6f2fb-116">В этом примере создается файл пакета развертывания (CSPKG) в каталоге службы и не публикуется в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="6f2fb-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2fb-117">PARAMETERS</span></span>

### <span data-ttu-id="6f2fb-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="6f2fb-118">-AffinityGroup</span></span>
<span data-ttu-id="6f2fb-119">Указывает территориальную группу, которую должна использовать служба.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-120">-Configuration</span><span class="sxs-lookup"><span data-stu-id="6f2fb-120">-Configuration</span></span>
<span data-ttu-id="6f2fb-121">Указывает файл конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="6f2fb-122">Если указать этот параметр, укажите параметр *Package* .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="6f2fb-123">-DeploymentName</span></span>
<span data-ttu-id="6f2fb-124">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="6f2fb-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-126">-Launch</span><span class="sxs-lookup"><span data-stu-id="6f2fb-126">-Launch</span></span>
<span data-ttu-id="6f2fb-127">Открывает окно браузера, чтобы можно было просмотреть приложение после его развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-128">-Location</span><span class="sxs-lookup"><span data-stu-id="6f2fb-128">-Location</span></span>
<span data-ttu-id="6f2fb-129">Область, в которой будет размещено приложение.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="6f2fb-130">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6f2fb-130">Possible values are:</span></span> 
  
- <span data-ttu-id="6f2fb-131">В любом уголке Азии</span><span class="sxs-lookup"><span data-stu-id="6f2fb-131">Anywhere Asia</span></span>
- <span data-ttu-id="6f2fb-132">В любом уголке Европы</span><span class="sxs-lookup"><span data-stu-id="6f2fb-132">Anywhere Europe</span></span>
- <span data-ttu-id="6f2fb-133">Где бы мы ни находились</span><span class="sxs-lookup"><span data-stu-id="6f2fb-133">Anywhere US</span></span>
- <span data-ttu-id="6f2fb-134">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6f2fb-134">East Asia</span></span>
- <span data-ttu-id="6f2fb-135">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="6f2fb-135">East US</span></span>
- <span data-ttu-id="6f2fb-136">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="6f2fb-136">North Central US</span></span>
- <span data-ttu-id="6f2fb-137">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="6f2fb-137">North Europe</span></span>
- <span data-ttu-id="6f2fb-138">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="6f2fb-138">South Central US</span></span>
- <span data-ttu-id="6f2fb-139">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="6f2fb-139">Southeast Asia</span></span>
- <span data-ttu-id="6f2fb-140">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="6f2fb-140">West Europe</span></span>
- <span data-ttu-id="6f2fb-141">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="6f2fb-141">West US</span></span>
 
<span data-ttu-id="6f2fb-142">Если расположение не указано, будет использоваться расположение, указанное в последнем вызове **Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="6f2fb-143">Если вы не указали расположение, оно будет выбрано случайным образом из расположений "Северный центр США" и "Южная Центральная США".</span><span class="sxs-lookup"><span data-stu-id="6f2fb-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-144">-Package</span><span class="sxs-lookup"><span data-stu-id="6f2fb-144">-Package</span></span>
<span data-ttu-id="6f2fb-145">Указывает файл пакета для развертывания.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="6f2fb-146">Укажите локальный файл, содержащий расширение имени файла cspkg или URI-код большого двоичного объекта, содержащего пакет.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="6f2fb-147">Если вы задаете этот параметр, не указывайте параметр *ServiceName* .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="6f2fb-148">-Profile</span></span>
<span data-ttu-id="6f2fb-149">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6f2fb-150">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6f2fb-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6f2fb-151">-ServiceName</span></span>
<span data-ttu-id="6f2fb-152">Указывает имя, которое будет использоваться службой при публикации в Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="6f2fb-153">Имя определяет часть метки в дочернем домене cloudapp.net, которая используется для адресации службы при размещении в Windows Azure (то есть **Name**. cloudapp.NET).</span><span class="sxs-lookup"><span data-stu-id="6f2fb-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="6f2fb-154">Имя, указанное при публикации, переопределяет имя, указанное при создании службы.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="6f2fb-155">(Дополнительные сведения о командлете **New-AzureServiceProject** ).</span><span class="sxs-lookup"><span data-stu-id="6f2fb-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f2fb-156">-Slot</span></span>
<span data-ttu-id="6f2fb-157">Слот развертывания, который будет использоваться для этой службы.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="6f2fb-158">Возможные значения: "промежуточные и производственные".</span><span class="sxs-lookup"><span data-stu-id="6f2fb-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="6f2fb-159">Если ячейка не указана, используется гнездо, указанное в последнем вызове Set-AzureDeploymentSlot.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="6f2fb-160">Если слот не указан, используется гнездо "производство".</span><span class="sxs-lookup"><span data-stu-id="6f2fb-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f2fb-161">-StorageAccountName</span></span>
<span data-ttu-id="6f2fb-162">Указывает имя учетной записи хранения Windows Azure, которое будет использоваться при публикации службы.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="6f2fb-163">Это значение не используется, пока служба не опубликована.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="6f2fb-164">Если этот параметр не указан, значение извлекается из последней команды **Set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="6f2fb-165">Если учетная запись хранения не была указана, будет использоваться учетная запись хранилища, соответствующая имени службы.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="6f2fb-166">Если такой учетной записи хранения не существует, командлет попытается создать новый.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="6f2fb-167">Однако попытка может завершиться ошибкой, если учетная запись хранения, совпадающая с именем службы, существует в другой подписке.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f2fb-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2fb-168">CommonParameters</span></span>
<span data-ttu-id="6f2fb-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f2fb-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2fb-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2fb-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2fb-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f2fb-171">INPUTS</span></span>

## <span data-ttu-id="6f2fb-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2fb-172">OUTPUTS</span></span>

## <span data-ttu-id="6f2fb-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f2fb-173">NOTES</span></span>

## <span data-ttu-id="6f2fb-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2fb-174">RELATED LINKS</span></span>

[<span data-ttu-id="6f2fb-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="6f2fb-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="6f2fb-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="6f2fb-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


