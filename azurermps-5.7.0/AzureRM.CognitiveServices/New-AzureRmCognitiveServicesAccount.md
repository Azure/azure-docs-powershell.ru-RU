---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 1c1d4ad776ed3db2cb3b5adfb490902a7de12f42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732168"
---
# <span data-ttu-id="1ec1d-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1ec1d-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="1ec1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ec1d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec1d-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ec1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ec1d-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ec1d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec1d-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec1d-106">Командлет **New-AzureRmCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="1ec1d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ec1d-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec1d-108">1:</span><span class="sxs-lookup"><span data-stu-id="1ec1d-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="1ec1d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec1d-109">PARAMETERS</span></span>

### <span data-ttu-id="1ec1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec1d-110">-DefaultProfile</span></span>
<span data-ttu-id="1ec1d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ec1d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1ec1d-112">-Force</span></span>
<span data-ttu-id="1ec1d-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ec1d-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1ec1d-114">-Location</span></span>
<span data-ttu-id="1ec1d-115">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-115">Specifies the location in which to create the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ec1d-116">-Name</span></span>
<span data-ttu-id="1ec1d-117">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-117">Specifies the name for the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec1d-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ec1d-119">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-119">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="1ec1d-120">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-120">The resource group must already exist.</span></span>

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

### <span data-ttu-id="1ec1d-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1ec1d-121">-SkuName</span></span>
<span data-ttu-id="1ec1d-122">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-122">Specifies the SKU for the account.</span></span>
<span data-ttu-id="1ec1d-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="1ec1d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ec1d-124">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="1ec1d-124">F0 (free tier)</span></span>
- <span data-ttu-id="1ec1d-125">S0</span><span class="sxs-lookup"><span data-stu-id="1ec1d-125">S0</span></span>
- <span data-ttu-id="1ec1d-126">Состояний</span><span class="sxs-lookup"><span data-stu-id="1ec1d-126">S1</span></span>
- <span data-ttu-id="1ec1d-127">S2</span><span class="sxs-lookup"><span data-stu-id="1ec1d-127">S2</span></span>
- <span data-ttu-id="1ec1d-128">Режима</span><span class="sxs-lookup"><span data-stu-id="1ec1d-128">S3</span></span>
- <span data-ttu-id="1ec1d-129">Режим</span><span class="sxs-lookup"><span data-stu-id="1ec1d-129">S4</span></span>

<span data-ttu-id="1ec1d-130">Дополнительные сведения можно найти в разделе [интерфейсы API службы для функций](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="1ec1d-130">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="1ec1d-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="1ec1d-131">-Tag</span></span>
<span data-ttu-id="1ec1d-132">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-132">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-133">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="1ec1d-133">-Type</span></span>
<span data-ttu-id="1ec1d-134">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-134">Specifies the type of account to create.</span></span> <span data-ttu-id="1ec1d-135">Текущие допустимые значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="1ec1d-135">Current acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ec1d-136">Bing. Автозаполнение. v7</span><span class="sxs-lookup"><span data-stu-id="1ec1d-136">Bing.Autosuggest.v7</span></span>
- <span data-ttu-id="1ec1d-137">Bing. CustomSearch</span><span class="sxs-lookup"><span data-stu-id="1ec1d-137">Bing.CustomSearch</span></span>
- <span data-ttu-id="1ec1d-138">Bing. Search. v7</span><span class="sxs-lookup"><span data-stu-id="1ec1d-138">Bing.Search.v7</span></span>
- <span data-ttu-id="1ec1d-139">Bing. Speech</span><span class="sxs-lookup"><span data-stu-id="1ec1d-139">Bing.Speech</span></span>
- <span data-ttu-id="1ec1d-140">Проверка правописания. v7</span><span class="sxs-lookup"><span data-stu-id="1ec1d-140">Bing.SpellCheck.v7</span></span>
- <span data-ttu-id="1ec1d-141">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="1ec1d-141">ComputerVision</span></span>
- <span data-ttu-id="1ec1d-142">ContentModerator</span><span class="sxs-lookup"><span data-stu-id="1ec1d-142">ContentModerator</span></span>
- <span data-ttu-id="1ec1d-143">CustomSpeech</span><span class="sxs-lookup"><span data-stu-id="1ec1d-143">CustomSpeech</span></span>
- <span data-ttu-id="1ec1d-144">CustomVision. PREDICTION</span><span class="sxs-lookup"><span data-stu-id="1ec1d-144">CustomVision.Prediction</span></span>
- <span data-ttu-id="1ec1d-145">CustomVision. Training</span><span class="sxs-lookup"><span data-stu-id="1ec1d-145">CustomVision.Training</span></span>
- <span data-ttu-id="1ec1d-146">Emotion</span><span class="sxs-lookup"><span data-stu-id="1ec1d-146">Emotion</span></span>
- <span data-ttu-id="1ec1d-147">Личные</span><span class="sxs-lookup"><span data-stu-id="1ec1d-147">Face</span></span>
- <span data-ttu-id="1ec1d-148">LUIS</span><span class="sxs-lookup"><span data-stu-id="1ec1d-148">LUIS</span></span>
- <span data-ttu-id="1ec1d-149">QnAMaker</span><span class="sxs-lookup"><span data-stu-id="1ec1d-149">QnAMaker</span></span>
- <span data-ttu-id="1ec1d-150">SpeakerRecognition</span><span class="sxs-lookup"><span data-stu-id="1ec1d-150">SpeakerRecognition</span></span>
- <span data-ttu-id="1ec1d-151">SpeechTranslation</span><span class="sxs-lookup"><span data-stu-id="1ec1d-151">SpeechTranslation</span></span>
- <span data-ttu-id="1ec1d-152">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="1ec1d-152">TextAnalytics</span></span>
- <span data-ttu-id="1ec1d-153">TextTranslation</span><span class="sxs-lookup"><span data-stu-id="1ec1d-153">TextTranslation</span></span>
- <span data-ttu-id="1ec1d-154">WebLM</span><span class="sxs-lookup"><span data-stu-id="1ec1d-154">WebLM</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ec1d-155">-Confirm</span></span>
<span data-ttu-id="1ec1d-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec1d-157">-WhatIf</span></span>
<span data-ttu-id="1ec1d-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec1d-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ec1d-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec1d-160">CommonParameters</span></span>
<span data-ttu-id="1ec1d-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec1d-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec1d-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec1d-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ec1d-163">INPUTS</span></span>

### <span data-ttu-id="1ec1d-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="1ec1d-164">None</span></span>
<span data-ttu-id="1ec1d-165">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1ec1d-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ec1d-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec1d-166">OUTPUTS</span></span>

### <span data-ttu-id="1ec1d-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1ec1d-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="1ec1d-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ec1d-168">NOTES</span></span>

## <span data-ttu-id="1ec1d-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec1d-169">RELATED LINKS</span></span>

[<span data-ttu-id="1ec1d-170">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1ec1d-170">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1ec1d-171">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1ec1d-171">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1ec1d-172">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1ec1d-172">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
