---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075950"
---
# <span data-ttu-id="764ed-101">Set-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="764ed-101">Set-AzureSubscription</span></span>

## <span data-ttu-id="764ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="764ed-102">SYNOPSIS</span></span>
<span data-ttu-id="764ed-103">Изменение подписки на Azure.</span><span class="sxs-lookup"><span data-stu-id="764ed-103">Changes an Azure subscription.</span></span>

## <span data-ttu-id="764ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="764ed-104">SYNTAX</span></span>

### <span data-ttu-id="764ed-105">UpdateSubscriptionByIdParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="764ed-105">UpdateSubscriptionByIdParameterSetName (Default)</span></span>
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="764ed-106">UpdateSubscriptionByNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="764ed-106">UpdateSubscriptionByNameParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="764ed-107">AddSubscriptionParameterSetName</span><span class="sxs-lookup"><span data-stu-id="764ed-107">AddSubscriptionParameterSetName</span></span>
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="764ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="764ed-108">DESCRIPTION</span></span>
<span data-ttu-id="764ed-109">Командлет **Set-AzureSubscription** устанавливает и изменяет свойства объекта подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="764ed-109">The **Set-AzureSubscription** cmdlet establishes and changes the properties of an Azure subscription object.</span></span>
<span data-ttu-id="764ed-110">Вы можете использовать этот командлет для работы в подписке Azure, не подписке по умолчанию, или изменить текущую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="764ed-110">You can use this cmdlet to work in an Azure subscription that is not your default subscription or to change your current storage account.</span></span>
<span data-ttu-id="764ed-111">Сведения о текущих подписок и подписках по умолчанию можно найти в командлете **SELECT-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="764ed-111">For information about current and default subscriptions, see the **Select-AzureSubscription** cmdlet.</span></span>

<span data-ttu-id="764ed-112">Этот командлет работает на объекте подписки Azure, а не в реальной подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="764ed-112">This cmdlet operates on an Azure subscription object, not your actual Azure subscription.</span></span>
<span data-ttu-id="764ed-113">Чтобы создать и подготовить подписку Azure, посетите [портал Azure](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="764ed-113">To create and provision an Azure subscription, visit the [Azure Portal](https://azure.microsoft.com/) (https://azure.microsoft.com/).</span></span>

<span data-ttu-id="764ed-114">Этот командлет изменяет данные в файле данных подписки, который создается при использовании командлета **Add-AzureAccount** или **Import-AzurePublishSettingsFile** для добавления учетной записи Azure в Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="764ed-114">This cmdlet changes the data in the subscription data file that you create when you use the **Add-AzureAccount** or **Import-AzurePublishSettingsFile** cmdlet to add an Azure account to Windows PowerShell.</span></span>

<span data-ttu-id="764ed-115">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="764ed-115">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="764ed-116">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="764ed-116">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="764ed-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="764ed-117">EXAMPLES</span></span>

### <span data-ttu-id="764ed-118">Пример 1: изменение существующего subscription1</span><span class="sxs-lookup"><span data-stu-id="764ed-118">Example 1: Change an existing subscription1</span></span>
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

<span data-ttu-id="764ed-119">В этом примере изменяется сертификат для подписки с именем ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="764ed-119">This example changes the certificate for the subscription named ContosoEngineering.</span></span>

### <span data-ttu-id="764ed-120">Пример 2: изменение конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="764ed-120">Example 2: Change the service endpoint</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

<span data-ttu-id="764ed-121">Эта команда добавляет или изменяет конечную точку настраиваемой службы для подписки на ContosoEngineering.</span><span class="sxs-lookup"><span data-stu-id="764ed-121">This command adds or changes a custom service endpoint for the ContosoEngineering subscription.</span></span>

### <span data-ttu-id="764ed-122">Пример 3: очистка значений свойств</span><span class="sxs-lookup"><span data-stu-id="764ed-122">Example 3: Clear property values</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

<span data-ttu-id="764ed-123">Эта команда задает значения NULL для параметров сертификата и ResourceManagerEndpoint ($Null).</span><span class="sxs-lookup"><span data-stu-id="764ed-123">This command sets the values of the Certificate and ResourceManagerEndpoint properties to null ($Null).</span></span>
<span data-ttu-id="764ed-124">При этом значения этих свойств удаляются без изменения других параметров.</span><span class="sxs-lookup"><span data-stu-id="764ed-124">This clears the values of those properties without changing other settings.</span></span>

### <span data-ttu-id="764ed-125">Пример 4: использование альтернативного файла данных подписки</span><span class="sxs-lookup"><span data-stu-id="764ed-125">Example 4: Use an alternate subscription data file</span></span>
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

<span data-ttu-id="764ed-126">Эта команда изменяет текущую учетную запись хранения для подписки на ContosoFinance на ContosoStorage01.</span><span class="sxs-lookup"><span data-stu-id="764ed-126">This command changes the current storage account of the ContosoFinance subscription to ContosoStorage01.</span></span>
<span data-ttu-id="764ed-127">Команда использует параметр **SubscriptionDataFile** для изменения данных в файле данных подписки C:\Azure\SubscriptionData.xml.</span><span class="sxs-lookup"><span data-stu-id="764ed-127">The command uses the **SubscriptionDataFile** parameter to change the data in the C:\Azure\SubscriptionData.xml subscription data file.</span></span>
<span data-ttu-id="764ed-128">По умолчанию для **Set-AzureSubscription** используется файл данных подписки по умолчанию в перемещаемом профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="764ed-128">By default, **Set-AzureSubscription** uses the default subscription data file in your roaming user profile.</span></span>

## <span data-ttu-id="764ed-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="764ed-129">PARAMETERS</span></span>

### <span data-ttu-id="764ed-130">-Certificate</span><span class="sxs-lookup"><span data-stu-id="764ed-130">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-131">-Context</span><span class="sxs-lookup"><span data-stu-id="764ed-131">-Context</span></span>
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-132">-CurrentStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="764ed-132">-CurrentStorageAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-133">-Environment</span><span class="sxs-lookup"><span data-stu-id="764ed-133">-Environment</span></span>
<span data-ttu-id="764ed-134">Указывает среду Azure.</span><span class="sxs-lookup"><span data-stu-id="764ed-134">Specifies an Azure environment.</span></span>

<span data-ttu-id="764ed-135">Среда Azure является независимым развертыванием Microsoft Azure, например AzureCloud для глобальных Azure и AzureChinaCloud для Azure, предоставляемой компанией 21Vianet в Китае.</span><span class="sxs-lookup"><span data-stu-id="764ed-135">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="764ed-136">Вы также можете создавать локальные среды Azure с помощью пакета Azure и командлетов WAPack.</span><span class="sxs-lookup"><span data-stu-id="764ed-136">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="764ed-137">Дополнительные сведения можно найти в [пакете Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="764ed-137">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="764ed-138">-PassThru</span></span>
<span data-ttu-id="764ed-139">Возвращает $True, если команда выполнена успешно, и $False в случае ее сбоя.</span><span class="sxs-lookup"><span data-stu-id="764ed-139">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="764ed-140">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="764ed-140">By default, this cmdlet does not return any output.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="764ed-141">-Profile</span></span>
<span data-ttu-id="764ed-142">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="764ed-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="764ed-143">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="764ed-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="764ed-144">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="764ed-144">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="764ed-145">Задает конечную точку для данных диспетчера ресурсов Azure, включая данные о группах ресурсов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="764ed-145">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="764ed-146">Дополнительные сведения об диспетчере ресурсов Azure можно найти в [командлетах диспетчера ресурсов Azure](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) и [с помощью Windows PowerShell с диспетчером ресурсов](https://go.microsoft.com/fwlink/?LinkID=394767)  ) ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="764ed-146">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="764ed-147">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="764ed-147">-ServiceEndpoint</span></span>
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

### <span data-ttu-id="764ed-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="764ed-148">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-149">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="764ed-149">-SubscriptionName</span></span>
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="764ed-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764ed-150">CommonParameters</span></span>
<span data-ttu-id="764ed-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="764ed-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764ed-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764ed-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764ed-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="764ed-153">INPUTS</span></span>

### <span data-ttu-id="764ed-154">Ничего</span><span class="sxs-lookup"><span data-stu-id="764ed-154">None</span></span>
<span data-ttu-id="764ed-155">Вы можете передавать входные данные командлету по имени свойства, но не по значению.</span><span class="sxs-lookup"><span data-stu-id="764ed-155">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="764ed-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="764ed-156">OUTPUTS</span></span>

### <span data-ttu-id="764ed-157">None и System. Boolean</span><span class="sxs-lookup"><span data-stu-id="764ed-157">None or System.Boolean</span></span>
<span data-ttu-id="764ed-158">При использовании параметра *PassThru* этот командлет возвращает логическое значение.</span><span class="sxs-lookup"><span data-stu-id="764ed-158">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="764ed-159">По умолчанию этот командлет не возвращает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="764ed-159">By default, this cmdlet does not return any output.</span></span>

## <span data-ttu-id="764ed-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="764ed-160">NOTES</span></span>

## <span data-ttu-id="764ed-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="764ed-161">RELATED LINKS</span></span>

[<span data-ttu-id="764ed-162">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="764ed-162">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="764ed-163">Get-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="764ed-163">Get-AzureSubscription</span></span>](./Get-AzureSubscription.md)

[<span data-ttu-id="764ed-164">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="764ed-164">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="764ed-165">Remove-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="764ed-165">Remove-AzureSubscription</span></span>](./Remove-AzureSubscription.md)

[<span data-ttu-id="764ed-166">SELECT-AzureSubscription</span><span class="sxs-lookup"><span data-stu-id="764ed-166">Select-AzureSubscription</span></span>](./Select-AzureSubscription.md)


