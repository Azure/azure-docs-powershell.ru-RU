---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229164"
---
# <span data-ttu-id="79c5a-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="79c5a-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="79c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="79c5a-103">Получает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="79c5a-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="79c5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79c5a-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c5a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c5a-105">DESCRIPTION</span></span>
<span data-ttu-id="79c5a-106">Cmdlet **Get-AzCognitiveServicesAccountKey** получает ключи API для учетной записи provisioned Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="79c5a-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="79c5a-107">Учетная запись когнитивных служб имеет два ключа API: "Ключ1" и "Ключ2".</span><span class="sxs-lookup"><span data-stu-id="79c5a-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="79c5a-108">Эти клавиши обеспечивают взаимодействие с конечной точкой учетной записи учетной записи "Когнитивные услуги".</span><span class="sxs-lookup"><span data-stu-id="79c5a-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="79c5a-109">Используйте New-AzCognitiveServicesAccountKey для повторного сгенерации ключа.</span><span class="sxs-lookup"><span data-stu-id="79c5a-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="79c5a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="79c5a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79c5a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="79c5a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79c5a-112">PARAMETERS</span></span>

### <span data-ttu-id="79c5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c5a-113">-DefaultProfile</span></span>
<span data-ttu-id="79c5a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="79c5a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79c5a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="79c5a-115">-Name</span></span>
<span data-ttu-id="79c5a-116">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="79c5a-116">Specifies the name of the account.</span></span>
<span data-ttu-id="79c5a-117">Этот cmdlet получает ключи для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="79c5a-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="79c5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="79c5a-119">Имя группы ресурсов, назначенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="79c5a-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="79c5a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c5a-120">CommonParameters</span></span>
<span data-ttu-id="79c5a-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c5a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c5a-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79c5a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c5a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79c5a-123">INPUTS</span></span>

### <span data-ttu-id="79c5a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="79c5a-124">System.String</span></span>

## <span data-ttu-id="79c5a-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79c5a-125">OUTPUTS</span></span>

### <span data-ttu-id="79c5a-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="79c5a-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="79c5a-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79c5a-127">NOTES</span></span>

## <span data-ttu-id="79c5a-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79c5a-128">RELATED LINKS</span></span>

[<span data-ttu-id="79c5a-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="79c5a-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


