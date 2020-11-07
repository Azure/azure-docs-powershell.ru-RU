---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: 05c5e797fa5ed56d6397b3881b368038a3d03a4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731390"
---
# <span data-ttu-id="3724b-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="3724b-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="3724b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3724b-102">SYNOPSIS</span></span>
<span data-ttu-id="3724b-103">Получает доступные типы учетных записей для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3724b-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="3724b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3724b-104">SYNTAX</span></span>

### <span data-ttu-id="3724b-105">GetAccountTypes (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3724b-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3724b-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="3724b-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3724b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3724b-107">DESCRIPTION</span></span>
<span data-ttu-id="3724b-108">Командлет **Get-AzCognitiveServicesAccountType** получает доступные типы учетных записей для автоматического перезаписи в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="3724b-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="3724b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3724b-109">EXAMPLES</span></span>

### <span data-ttu-id="3724b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3724b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="3724b-111">Получение списка доступных типов.</span><span class="sxs-lookup"><span data-stu-id="3724b-111">Get the list of available Types.</span></span>

### <span data-ttu-id="3724b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3724b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="3724b-113">Получение списка доступных типов в westus.</span><span class="sxs-lookup"><span data-stu-id="3724b-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="3724b-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3724b-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="3724b-115">Убедитесь, что имя `Face` типа является допустимым, и оно будет возвращено, если оно является допустимым именем.</span><span class="sxs-lookup"><span data-stu-id="3724b-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="3724b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3724b-116">PARAMETERS</span></span>

### <span data-ttu-id="3724b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3724b-117">-DefaultProfile</span></span>
<span data-ttu-id="3724b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3724b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3724b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3724b-119">-Location</span></span>
<span data-ttu-id="3724b-120">Расположение учетной записи для пересчета служб.</span><span class="sxs-lookup"><span data-stu-id="3724b-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="3724b-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="3724b-121">-TypeName</span></span>
<span data-ttu-id="3724b-122">Имя типа учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3724b-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="3724b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3724b-123">CommonParameters</span></span>
<span data-ttu-id="3724b-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3724b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3724b-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3724b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3724b-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3724b-126">INPUTS</span></span>

### <span data-ttu-id="3724b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3724b-127">System.String</span></span>

## <span data-ttu-id="3724b-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3724b-128">OUTPUTS</span></span>

### <span data-ttu-id="3724b-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="3724b-129">System.String[]</span></span>

### <span data-ttu-id="3724b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3724b-130">System.String</span></span>

## <span data-ttu-id="3724b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3724b-131">NOTES</span></span>

## <span data-ttu-id="3724b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3724b-132">RELATED LINKS</span></span>
