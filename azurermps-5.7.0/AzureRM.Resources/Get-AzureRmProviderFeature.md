---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: d13eb98b01380fcb02392d1ac3f34c8d70c7f6dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733550"
---
# <span data-ttu-id="f7413-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f7413-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="f7413-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7413-102">SYNOPSIS</span></span>
<span data-ttu-id="f7413-103">Получение сведений о возможностях поставщика Azure.</span><span class="sxs-lookup"><span data-stu-id="f7413-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7413-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7413-104">SYNTAX</span></span>

### <span data-ttu-id="f7413-105">ListAvailableParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7413-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7413-106">Функция функцию</span><span class="sxs-lookup"><span data-stu-id="f7413-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7413-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7413-107">DESCRIPTION</span></span>
<span data-ttu-id="f7413-108">Командлет **Get-AzureRmProviderFeature** получает имя компонента, имя поставщика и состояние регистрации для функций поставщика Azure.</span><span class="sxs-lookup"><span data-stu-id="f7413-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="f7413-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7413-109">EXAMPLES</span></span>

### <span data-ttu-id="f7413-110">Пример 1: получение всех доступных функций</span><span class="sxs-lookup"><span data-stu-id="f7413-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="f7413-111">Эта команда получает все доступные функции.</span><span class="sxs-lookup"><span data-stu-id="f7413-111">This command gets all available features.</span></span>

### <span data-ttu-id="f7413-112">Пример 2: получение сведений о конкретном компоненте</span><span class="sxs-lookup"><span data-stu-id="f7413-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="f7413-113">Эта команда получает сведения о компоненте с именем AllowPreReleaseRegions для указанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7413-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="f7413-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7413-114">PARAMETERS</span></span>

### <span data-ttu-id="f7413-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7413-115">-DefaultProfile</span></span>
<span data-ttu-id="f7413-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7413-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7413-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="f7413-117">-FeatureName</span></span>
<span data-ttu-id="f7413-118">Указывает имя компонента, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f7413-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7413-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="f7413-119">-ListAvailable</span></span>
<span data-ttu-id="f7413-120">Указывает на то, что этот командлет получает все компоненты.</span><span class="sxs-lookup"><span data-stu-id="f7413-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7413-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f7413-121">-ProviderNamespace</span></span>
<span data-ttu-id="f7413-122">Задает пространство имен, для которого этот командлет получает функции поставщика.</span><span class="sxs-lookup"><span data-stu-id="f7413-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7413-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7413-123">CommonParameters</span></span>
<span data-ttu-id="f7413-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7413-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7413-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7413-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7413-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7413-126">INPUTS</span></span>

### <span data-ttu-id="f7413-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7413-127">None</span></span>
<span data-ttu-id="f7413-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7413-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7413-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7413-129">OUTPUTS</span></span>

### <span data-ttu-id="f7413-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="f7413-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="f7413-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7413-131">NOTES</span></span>

## <span data-ttu-id="f7413-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7413-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7413-133">Регистрация — AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f7413-133">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


