---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: f9b9f48d671bd0cbae0b7f8a26eccb21f372c4ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565619"
---
# <span data-ttu-id="72030-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="72030-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="72030-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="72030-102">SYNOPSIS</span></span>
<span data-ttu-id="72030-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="72030-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72030-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="72030-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72030-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72030-105">DESCRIPTION</span></span>
<span data-ttu-id="72030-106">Командлет **Get-AzureRmCognitiveServicesAccountKey** получает ключи API для учетной записи настроенных персонализированных служб.</span><span class="sxs-lookup"><span data-stu-id="72030-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="72030-107">Учетная запись службы использует два ключа API: key1 и Key2.</span><span class="sxs-lookup"><span data-stu-id="72030-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="72030-108">Ключи обеспечивают взаимодействие с конечной точкой учетной записи самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="72030-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="72030-109">Для повторного создания ключа используйте New-AzureRmCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="72030-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="72030-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="72030-110">EXAMPLES</span></span>

## <span data-ttu-id="72030-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="72030-111">PARAMETERS</span></span>

### <span data-ttu-id="72030-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="72030-112">-Name</span></span>
<span data-ttu-id="72030-113">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="72030-113">Specifies the name of the account.</span></span>
<span data-ttu-id="72030-114">Этот командлет получает ключи для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="72030-114">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="72030-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72030-115">-ResourceGroupName</span></span>
<span data-ttu-id="72030-116">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="72030-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="72030-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72030-117">-DefaultProfile</span></span>
<span data-ttu-id="72030-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72030-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72030-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72030-119">CommonParameters</span></span>
<span data-ttu-id="72030-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="72030-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72030-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72030-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72030-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="72030-122">INPUTS</span></span>

## <span data-ttu-id="72030-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="72030-123">OUTPUTS</span></span>

### <span data-ttu-id="72030-124">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="72030-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="72030-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="72030-125">NOTES</span></span>

## <span data-ttu-id="72030-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72030-126">RELATED LINKS</span></span>

[<span data-ttu-id="72030-127">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="72030-127">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


