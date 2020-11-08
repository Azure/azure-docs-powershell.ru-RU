---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075929"
---
# <span data-ttu-id="c767d-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c767d-101">New-AzureDeployment</span></span>

## <span data-ttu-id="c767d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c767d-102">SYNOPSIS</span></span>
<span data-ttu-id="c767d-103">Создает развертывание из службы.</span><span class="sxs-lookup"><span data-stu-id="c767d-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="c767d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c767d-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c767d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c767d-105">DESCRIPTION</span></span>
<span data-ttu-id="c767d-106">Командлет **New-AzureDeployment** создает развертывание Azure из службы, которая включает веб-роли и рабочие роли.</span><span class="sxs-lookup"><span data-stu-id="c767d-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="c767d-107">Этот командлет создает развертывание на основе файла пакета (CSPKG) и файла конфигурации службы (cscfg).</span><span class="sxs-lookup"><span data-stu-id="c767d-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="c767d-108">Укажите имя, уникальное в среде развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="c767d-109">Используйте командлет **New-AzureVM** для создания развертывания на основе виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="c767d-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="c767d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c767d-110">EXAMPLES</span></span>

### <span data-ttu-id="c767d-111">Пример 1: создание развертывания</span><span class="sxs-lookup"><span data-stu-id="c767d-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="c767d-112">Эта команда создает рабочее развертывание на основе пакета с именем ContosoPackage. cspkg и конфигурации с именем ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="c767d-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="c767d-113">Команда задает метку для развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="c767d-114">Имя не указывается.</span><span class="sxs-lookup"><span data-stu-id="c767d-114">It does not specify a name.</span></span>
<span data-ttu-id="c767d-115">Этот командлет создает GUID в качестве имени.</span><span class="sxs-lookup"><span data-stu-id="c767d-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="c767d-116">Пример 2: создание развертывания на основе конфигурации расширения</span><span class="sxs-lookup"><span data-stu-id="c767d-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="c767d-117">Эта команда создает рабочее развертывание на основе пакета и конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c767d-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="c767d-118">Команда задает конфигурацию расширения с именем ContosoExtensionConfig. cscfg.</span><span class="sxs-lookup"><span data-stu-id="c767d-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="c767d-119">Этот командлет создает идентификаторы GUID в качестве имени и метки.</span><span class="sxs-lookup"><span data-stu-id="c767d-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="c767d-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c767d-120">PARAMETERS</span></span>

### <span data-ttu-id="c767d-121">-Configuration</span><span class="sxs-lookup"><span data-stu-id="c767d-121">-Configuration</span></span>
<span data-ttu-id="c767d-122">Указывает полный путь к файлу конфигурации службы.</span><span class="sxs-lookup"><span data-stu-id="c767d-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="c767d-123">-DoNotStart</span></span>
<span data-ttu-id="c767d-124">Указывает, что этот командлет не запускает развертывание.</span><span class="sxs-lookup"><span data-stu-id="c767d-124">Specifies that this cmdlet does not start the deployment.</span></span>

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

### <span data-ttu-id="c767d-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="c767d-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="c767d-126">Задает массив объектов конфигурации расширения.</span><span class="sxs-lookup"><span data-stu-id="c767d-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c767d-127">-InformationAction</span></span>
<span data-ttu-id="c767d-128">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="c767d-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c767d-129">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c767d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c767d-130">Продолжал</span><span class="sxs-lookup"><span data-stu-id="c767d-130">Continue</span></span>
- <span data-ttu-id="c767d-131">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="c767d-131">Ignore</span></span>
- <span data-ttu-id="c767d-132">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="c767d-132">Inquire</span></span>
- <span data-ttu-id="c767d-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c767d-133">SilentlyContinue</span></span>
- <span data-ttu-id="c767d-134">Остановить</span><span class="sxs-lookup"><span data-stu-id="c767d-134">Stop</span></span>
- <span data-ttu-id="c767d-135">Рвать</span><span class="sxs-lookup"><span data-stu-id="c767d-135">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c767d-136">-InformationVariable</span></span>
<span data-ttu-id="c767d-137">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="c767d-137">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-138">-Label</span><span class="sxs-lookup"><span data-stu-id="c767d-138">-Label</span></span>
<span data-ttu-id="c767d-139">Указывает имя метки для развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="c767d-140">Если вы не укажете метку, этот командлет использует GUID.</span><span class="sxs-lookup"><span data-stu-id="c767d-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c767d-141">-Name</span></span>
<span data-ttu-id="c767d-142">Указывает имя развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-142">Specifies a deployment name.</span></span>
<span data-ttu-id="c767d-143">Если имя не задано, этот командлет использует GUID.</span><span class="sxs-lookup"><span data-stu-id="c767d-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-144">-Package</span><span class="sxs-lookup"><span data-stu-id="c767d-144">-Package</span></span>
<span data-ttu-id="c767d-145">Указывает путь или универсальный код ресурса (URI) cspkg-файла в хранилище в той же подписке или проекте.</span><span class="sxs-lookup"><span data-stu-id="c767d-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="c767d-146">-Profile</span></span>
<span data-ttu-id="c767d-147">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c767d-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c767d-148">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c767d-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c767d-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c767d-149">-ServiceName</span></span>
<span data-ttu-id="c767d-150">Указывает имя службы Azure для развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="c767d-151">-Slot</span></span>
<span data-ttu-id="c767d-152">Указывает среду, в которой этот командлет создает развертывание.</span><span class="sxs-lookup"><span data-stu-id="c767d-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="c767d-153">Допустимые значения: промежуточные и производственные.</span><span class="sxs-lookup"><span data-stu-id="c767d-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="c767d-154">Значением по умолчанию является "производство".</span><span class="sxs-lookup"><span data-stu-id="c767d-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c767d-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="c767d-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="c767d-156">Указывает, что предупреждающие сообщения представляют собой ошибки.</span><span class="sxs-lookup"><span data-stu-id="c767d-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="c767d-157">Если вы задаете этот параметр, предупреждающее сообщение приводит к сбою развертывания.</span><span class="sxs-lookup"><span data-stu-id="c767d-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

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

### <span data-ttu-id="c767d-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c767d-158">CommonParameters</span></span>
<span data-ttu-id="c767d-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c767d-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c767d-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c767d-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c767d-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c767d-161">INPUTS</span></span>

## <span data-ttu-id="c767d-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c767d-162">OUTPUTS</span></span>

## <span data-ttu-id="c767d-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="c767d-163">NOTES</span></span>

## <span data-ttu-id="c767d-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c767d-164">RELATED LINKS</span></span>

[<span data-ttu-id="c767d-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c767d-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="c767d-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="c767d-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="c767d-167">Move-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c767d-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="c767d-168">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c767d-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="c767d-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c767d-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="c767d-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="c767d-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


