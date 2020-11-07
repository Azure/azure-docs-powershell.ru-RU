---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: cc890bf13922069ac9f4d20d6a9e8d0c3aa04c94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910928"
---
# <span data-ttu-id="948b9-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="948b9-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="948b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="948b9-102">SYNOPSIS</span></span>
<span data-ttu-id="948b9-103">Возвращает поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="948b9-103">Gets a resource provider.</span></span>

## <span data-ttu-id="948b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="948b9-104">SYNTAX</span></span>

### <span data-ttu-id="948b9-105">ListAvailable (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="948b9-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="948b9-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="948b9-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="948b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="948b9-107">DESCRIPTION</span></span>
<span data-ttu-id="948b9-108">Командлет **Get-AzResourceProvider** Получает поставщик ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="948b9-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="948b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="948b9-109">EXAMPLES</span></span>

## <span data-ttu-id="948b9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="948b9-110">PARAMETERS</span></span>

### <span data-ttu-id="948b9-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="948b9-111">-ApiVersion</span></span>
<span data-ttu-id="948b9-112">Указывает версию API, поддерживаемую поставщиком ресурсов.</span><span class="sxs-lookup"><span data-stu-id="948b9-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="948b9-113">Вы можете выбрать версию, отличную от версии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="948b9-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="948b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948b9-114">-DefaultProfile</span></span>
<span data-ttu-id="948b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="948b9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="948b9-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="948b9-116">-ListAvailable</span></span>
<span data-ttu-id="948b9-117">Указывает на то, что эта операция получает все доступные поставщики ресурсов.</span><span class="sxs-lookup"><span data-stu-id="948b9-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="948b9-118">-Location</span><span class="sxs-lookup"><span data-stu-id="948b9-118">-Location</span></span>
<span data-ttu-id="948b9-119">Указывает расположение поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="948b9-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="948b9-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="948b9-120">-Pre</span></span>
<span data-ttu-id="948b9-121">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="948b9-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="948b9-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="948b9-122">-ProviderNamespace</span></span>
<span data-ttu-id="948b9-123">Задает пространство имен поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="948b9-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="948b9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948b9-124">CommonParameters</span></span>
<span data-ttu-id="948b9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="948b9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948b9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948b9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948b9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="948b9-127">INPUTS</span></span>

## <span data-ttu-id="948b9-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="948b9-128">OUTPUTS</span></span>

## <span data-ttu-id="948b9-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="948b9-129">NOTES</span></span>

## <span data-ttu-id="948b9-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="948b9-130">RELATED LINKS</span></span>

[<span data-ttu-id="948b9-131">Регистрация — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="948b9-131">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="948b9-132">Отмена регистрации — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="948b9-132">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


