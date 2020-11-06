---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: 54ce1d9fa73b29318597f5a1442712aabf7f92b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557191"
---
# <span data-ttu-id="0e9a3-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e9a3-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="0e9a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9a3-103">Возвращает поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e9a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e9a3-104">SYNTAX</span></span>

### <span data-ttu-id="0e9a3-105">ListAvailable (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e9a3-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e9a3-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="0e9a3-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e9a3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e9a3-107">DESCRIPTION</span></span>
<span data-ttu-id="0e9a3-108">Командлет **Get-AzureRmResourceProvider** Получает поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="0e9a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e9a3-109">EXAMPLES</span></span>

## <span data-ttu-id="0e9a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e9a3-110">PARAMETERS</span></span>

### <span data-ttu-id="0e9a3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0e9a3-111">-ApiVersion</span></span>
<span data-ttu-id="0e9a3-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="0e9a3-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="0e9a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e9a3-114">-DefaultProfile</span></span>
<span data-ttu-id="0e9a3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0e9a3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e9a3-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="0e9a3-116">-ListAvailable</span></span>
<span data-ttu-id="0e9a3-117">Указывает на то, что эта операция получает все доступные поставщики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9a3-118">-Location</span><span class="sxs-lookup"><span data-stu-id="0e9a3-118">-Location</span></span>
<span data-ttu-id="0e9a3-119">Указывает расположение поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="0e9a3-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="0e9a3-120">-Pre</span></span>
<span data-ttu-id="0e9a3-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0e9a3-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="0e9a3-122">-ProviderNamespace</span></span>
<span data-ttu-id="0e9a3-123">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: String
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9a3-124">CommonParameters</span></span>
<span data-ttu-id="0e9a3-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9a3-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9a3-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e9a3-127">INPUTS</span></span>

### <span data-ttu-id="0e9a3-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="0e9a3-128">None</span></span>
<span data-ttu-id="0e9a3-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0e9a3-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e9a3-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e9a3-130">OUTPUTS</span></span>

### <span data-ttu-id="0e9a3-131">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e9a3-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="0e9a3-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e9a3-132">NOTES</span></span>

## <span data-ttu-id="0e9a3-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e9a3-133">RELATED LINKS</span></span>

[<span data-ttu-id="0e9a3-134">Регистрация — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e9a3-134">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="0e9a3-135">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="0e9a3-135">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


