---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 449b10f851dbd4e2f2e804bab0772543d512c0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569700"
---
# <span data-ttu-id="f1258-101">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1258-101">New-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="f1258-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1258-102">SYNOPSIS</span></span>
<span data-ttu-id="f1258-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="f1258-103">Creates a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1258-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1258-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1258-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1258-105">DESCRIPTION</span></span>
<span data-ttu-id="f1258-106">Командлет **New-AzureRmCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="f1258-106">The **New-AzureRmCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="f1258-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1258-107">EXAMPLES</span></span>

### <span data-ttu-id="f1258-108">1:</span><span class="sxs-lookup"><span data-stu-id="f1258-108">1:</span></span>
```
New-AzureRmCognitiveServicesAccount -ResourceGroupName 'resourcegroup1' -name 'MyAccountName' -Type TextTranslation -SkuName F0 -Location 'usgovvirginia'
```

## <span data-ttu-id="f1258-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1258-109">PARAMETERS</span></span>

### <span data-ttu-id="f1258-110">-Force</span><span class="sxs-lookup"><span data-stu-id="f1258-110">-Force</span></span>
<span data-ttu-id="f1258-111">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f1258-111">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-112">-Location</span><span class="sxs-lookup"><span data-stu-id="f1258-112">-Location</span></span>
<span data-ttu-id="f1258-113">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1258-113">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f1258-114">-Name</span></span>
<span data-ttu-id="f1258-115">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1258-115">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1258-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1258-117">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f1258-117">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="f1258-118">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="f1258-118">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f1258-119">-SkuName</span></span>
<span data-ttu-id="f1258-120">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f1258-120">Specifies the SKU for the account.</span></span>
<span data-ttu-id="f1258-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f1258-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1258-122">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="f1258-122">F0 (free tier)</span></span>
- <span data-ttu-id="f1258-123">S0</span><span class="sxs-lookup"><span data-stu-id="f1258-123">S0</span></span>
- <span data-ttu-id="f1258-124">Состояний</span><span class="sxs-lookup"><span data-stu-id="f1258-124">S1</span></span>
- <span data-ttu-id="f1258-125">S2</span><span class="sxs-lookup"><span data-stu-id="f1258-125">S2</span></span>
- <span data-ttu-id="f1258-126">Режима</span><span class="sxs-lookup"><span data-stu-id="f1258-126">S3</span></span>
- <span data-ttu-id="f1258-127">Режим</span><span class="sxs-lookup"><span data-stu-id="f1258-127">S4</span></span>

<span data-ttu-id="f1258-128">Дополнительные сведения можно найти в разделе [интерфейсы API службы для функций](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="f1258-128">For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="f1258-129">-Tag</span></span>
<span data-ttu-id="f1258-130">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="f1258-130">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-131">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f1258-131">-Type</span></span>
<span data-ttu-id="f1258-132">Указывает тип создаваемой учетной записи. Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f1258-132">Specifies the type of account to create.The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f1258-133">ComputerVision</span><span class="sxs-lookup"><span data-stu-id="f1258-133">ComputerVision</span></span>
- <span data-ttu-id="f1258-134">Emotion</span><span class="sxs-lookup"><span data-stu-id="f1258-134">Emotion</span></span>
- <span data-ttu-id="f1258-135">Личные</span><span class="sxs-lookup"><span data-stu-id="f1258-135">Face</span></span>
- <span data-ttu-id="f1258-136">LUIS</span><span class="sxs-lookup"><span data-stu-id="f1258-136">LUIS</span></span>
- <span data-ttu-id="f1258-137">Советы</span><span class="sxs-lookup"><span data-stu-id="f1258-137">Recommendations</span></span>
- <span data-ttu-id="f1258-138">Речи</span><span class="sxs-lookup"><span data-stu-id="f1258-138">Speech</span></span>
- <span data-ttu-id="f1258-139">TextAnalytics</span><span class="sxs-lookup"><span data-stu-id="f1258-139">TextAnalytics</span></span>
- <span data-ttu-id="f1258-140">WebLM</span><span class="sxs-lookup"><span data-stu-id="f1258-140">WebLM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1258-141">-Confirm</span></span>
<span data-ttu-id="f1258-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1258-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1258-143">-WhatIf</span></span>
<span data-ttu-id="f1258-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1258-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1258-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1258-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1258-146">-DefaultProfile</span></span>
<span data-ttu-id="f1258-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1258-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1258-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1258-148">CommonParameters</span></span>
<span data-ttu-id="f1258-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1258-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1258-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1258-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1258-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1258-151">INPUTS</span></span>

## <span data-ttu-id="f1258-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1258-152">OUTPUTS</span></span>

### <span data-ttu-id="f1258-153">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1258-153">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="f1258-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1258-154">NOTES</span></span>

## <span data-ttu-id="f1258-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1258-155">RELATED LINKS</span></span>

[<span data-ttu-id="f1258-156">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1258-156">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="f1258-157">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1258-157">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="f1258-158">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f1258-158">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)
