---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913416"
---
# <span data-ttu-id="c026a-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c026a-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="c026a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c026a-102">SYNOPSIS</span></span>
<span data-ttu-id="c026a-103">Возвращает поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c026a-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c026a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c026a-104">SYNTAX</span></span>

### <span data-ttu-id="c026a-105">ListAvailable (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c026a-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c026a-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="c026a-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c026a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c026a-107">DESCRIPTION</span></span>
<span data-ttu-id="c026a-108">Командлет **Get-AzureRmResourceProvider** Получает поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c026a-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="c026a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c026a-109">EXAMPLES</span></span>

## <span data-ttu-id="c026a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c026a-110">PARAMETERS</span></span>

### <span data-ttu-id="c026a-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c026a-111">-ApiVersion</span></span>
<span data-ttu-id="c026a-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c026a-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="c026a-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c026a-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c026a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c026a-114">-DefaultProfile</span></span>
<span data-ttu-id="c026a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c026a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c026a-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c026a-116">-ListAvailable</span></span>
<span data-ttu-id="c026a-117">Указывает на то, что эта операция получает все доступные поставщики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c026a-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c026a-118">-Location</span><span class="sxs-lookup"><span data-stu-id="c026a-118">-Location</span></span>
<span data-ttu-id="c026a-119">Указывает расположение поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c026a-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c026a-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="c026a-120">-Pre</span></span>
<span data-ttu-id="c026a-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="c026a-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c026a-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c026a-122">-ProviderNamespace</span></span>
<span data-ttu-id="c026a-123">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c026a-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c026a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c026a-124">CommonParameters</span></span>
<span data-ttu-id="c026a-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c026a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c026a-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c026a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c026a-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c026a-127">INPUTS</span></span>

## <span data-ttu-id="c026a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c026a-128">OUTPUTS</span></span>

## <span data-ttu-id="c026a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c026a-129">NOTES</span></span>

## <span data-ttu-id="c026a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c026a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c026a-131">Регистрация — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c026a-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="c026a-132">Отмена регистрации — AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c026a-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


