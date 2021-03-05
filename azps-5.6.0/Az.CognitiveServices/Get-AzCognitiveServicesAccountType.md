---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981219"
---
# <span data-ttu-id="39c20-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="39c20-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="39c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c20-102">SYNOPSIS</span></span>
<span data-ttu-id="39c20-103">Возвращает доступные типы учетных записей когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="39c20-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="39c20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39c20-104">SYNTAX</span></span>

### <span data-ttu-id="39c20-105">GetAccountTypes (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39c20-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39c20-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="39c20-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39c20-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c20-107">DESCRIPTION</span></span>
<span data-ttu-id="39c20-108">Для этой подписки доступны типы учетных записей Учетных записей **Get-AzCognitiveServicesAccountType.**</span><span class="sxs-lookup"><span data-stu-id="39c20-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="39c20-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39c20-109">EXAMPLES</span></span>

### <span data-ttu-id="39c20-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39c20-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="39c20-111">Получить список доступных типов.</span><span class="sxs-lookup"><span data-stu-id="39c20-111">Get the list of available Types.</span></span>

### <span data-ttu-id="39c20-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="39c20-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="39c20-113">Получить список доступных типов на westus.</span><span class="sxs-lookup"><span data-stu-id="39c20-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="39c20-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="39c20-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="39c20-115">Проверьте, допустимо ли имя типа, оно будет возвращено, если `Face` оно допустимо.</span><span class="sxs-lookup"><span data-stu-id="39c20-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="39c20-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39c20-116">PARAMETERS</span></span>

### <span data-ttu-id="39c20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c20-117">-DefaultProfile</span></span>
<span data-ttu-id="39c20-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39c20-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c20-119">-Location</span><span class="sxs-lookup"><span data-stu-id="39c20-119">-Location</span></span>
<span data-ttu-id="39c20-120">Расположение учетной записи службы когнитивных функций.</span><span class="sxs-lookup"><span data-stu-id="39c20-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="39c20-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="39c20-121">-TypeName</span></span>
<span data-ttu-id="39c20-122">Имя типа учетной записи "Когнитивные услуги".</span><span class="sxs-lookup"><span data-stu-id="39c20-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="39c20-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c20-123">CommonParameters</span></span>
<span data-ttu-id="39c20-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39c20-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c20-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39c20-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c20-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39c20-126">INPUTS</span></span>

### <span data-ttu-id="39c20-127">System.String</span><span class="sxs-lookup"><span data-stu-id="39c20-127">System.String</span></span>

## <span data-ttu-id="39c20-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39c20-128">OUTPUTS</span></span>

### <span data-ttu-id="39c20-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="39c20-129">System.String[]</span></span>

### <span data-ttu-id="39c20-130">System.String</span><span class="sxs-lookup"><span data-stu-id="39c20-130">System.String</span></span>

## <span data-ttu-id="39c20-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39c20-131">NOTES</span></span>

## <span data-ttu-id="39c20-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39c20-132">RELATED LINKS</span></span>
