---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509309"
---
# <span data-ttu-id="c8ff9-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="c8ff9-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="c8ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ff9-103">Возвращает доступные типы учетных записей когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="c8ff9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8ff9-104">SYNTAX</span></span>

### <span data-ttu-id="c8ff9-105">GetAccountTypes (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8ff9-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8ff9-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="c8ff9-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8ff9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8ff9-107">DESCRIPTION</span></span>
<span data-ttu-id="c8ff9-108">Для этой подписки можно получить типы учетных записей **Get-AzCognitiveServicesAccountType.**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="c8ff9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8ff9-109">EXAMPLES</span></span>

### <span data-ttu-id="c8ff9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c8ff9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="c8ff9-111">Получить список доступных типов.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-111">Get the list of available Types.</span></span>

### <span data-ttu-id="c8ff9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8ff9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="c8ff9-113">Получить список доступных типов в западной части.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="c8ff9-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c8ff9-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="c8ff9-115">Проверьте, допустимо ли имя типа, оно будет возвращено, если `Face` оно допустимо.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="c8ff9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8ff9-116">PARAMETERS</span></span>

### <span data-ttu-id="c8ff9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ff9-117">-DefaultProfile</span></span>
<span data-ttu-id="c8ff9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8ff9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c8ff9-119">-Location</span></span>
<span data-ttu-id="c8ff9-120">Расположение учетной записи службы когнитивных функций.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="c8ff9-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="c8ff9-121">-TypeName</span></span>
<span data-ttu-id="c8ff9-122">Имя типа учетной записи "Когнитивные услуги".</span><span class="sxs-lookup"><span data-stu-id="c8ff9-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="c8ff9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ff9-123">CommonParameters</span></span>
<span data-ttu-id="c8ff9-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ff9-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8ff9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ff9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8ff9-126">INPUTS</span></span>

### <span data-ttu-id="c8ff9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c8ff9-127">System.String</span></span>

## <span data-ttu-id="c8ff9-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8ff9-128">OUTPUTS</span></span>

### <span data-ttu-id="c8ff9-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c8ff9-129">System.String[]</span></span>

### <span data-ttu-id="c8ff9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c8ff9-130">System.String</span></span>

## <span data-ttu-id="c8ff9-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8ff9-131">NOTES</span></span>

## <span data-ttu-id="c8ff9-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8ff9-132">RELATED LINKS</span></span>
