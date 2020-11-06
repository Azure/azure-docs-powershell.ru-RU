---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567290"
---
# <span data-ttu-id="3c970-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="3c970-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="3c970-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c970-102">SYNOPSIS</span></span>
<span data-ttu-id="3c970-103">Получает доступные типы учетных записей для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3c970-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c970-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c970-104">SYNTAX</span></span>

### <span data-ttu-id="3c970-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="3c970-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c970-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="3c970-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c970-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c970-107">DESCRIPTION</span></span>
<span data-ttu-id="3c970-108">Командлет **Get-AzureRmCognitiveServicesAccountType** получает доступные типы учетных записей для автоматического перезаписи в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="3c970-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="3c970-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c970-109">EXAMPLES</span></span>

### <span data-ttu-id="3c970-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c970-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="3c970-111">Получение списка доступных типов.</span><span class="sxs-lookup"><span data-stu-id="3c970-111">Get the list of available Types.</span></span>

### <span data-ttu-id="3c970-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c970-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="3c970-113">Получение списка доступных типов в westus.</span><span class="sxs-lookup"><span data-stu-id="3c970-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="3c970-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3c970-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="3c970-115">Убедитесь, что имя `Face` типа является допустимым, и оно будет возвращено, если оно является допустимым именем.</span><span class="sxs-lookup"><span data-stu-id="3c970-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="3c970-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c970-116">PARAMETERS</span></span>

### <span data-ttu-id="3c970-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c970-117">-DefaultProfile</span></span>
<span data-ttu-id="3c970-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c970-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c970-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3c970-119">-Location</span></span>
<span data-ttu-id="3c970-120">Расположение учетной записи для пересчета служб.</span><span class="sxs-lookup"><span data-stu-id="3c970-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c970-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="3c970-121">-TypeName</span></span>
<span data-ttu-id="3c970-122">Имя типа учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3c970-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c970-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c970-123">CommonParameters</span></span>
<span data-ttu-id="3c970-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c970-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c970-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c970-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c970-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c970-126">INPUTS</span></span>

### <span data-ttu-id="3c970-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3c970-127">System.String</span></span>

## <span data-ttu-id="3c970-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c970-128">OUTPUTS</span></span>

### <span data-ttu-id="3c970-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="3c970-129">System.String[]</span></span>

### <span data-ttu-id="3c970-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3c970-130">System.String</span></span>

## <span data-ttu-id="3c970-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c970-131">NOTES</span></span>

## <span data-ttu-id="3c970-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c970-132">RELATED LINKS</span></span>
