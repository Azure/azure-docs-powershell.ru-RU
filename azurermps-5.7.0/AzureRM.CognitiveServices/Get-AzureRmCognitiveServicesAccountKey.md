---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566231"
---
# <span data-ttu-id="3ce2c-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ce2c-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="3ce2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ce2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ce2c-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ce2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ce2c-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ce2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce2c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ce2c-106">Командлет **Get-AzureRmCognitiveServicesAccountKey** получает ключи API для учетной записи настроенных персонализированных служб.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="3ce2c-107">Учетная запись службы использует два ключа API: key1 и Key2.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="3ce2c-108">Ключи обеспечивают взаимодействие с конечной точкой учетной записи самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="3ce2c-109">Для повторного создания ключа используйте New-AzureRmCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="3ce2c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ce2c-110">EXAMPLES</span></span>

## <span data-ttu-id="3ce2c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ce2c-111">PARAMETERS</span></span>

### <span data-ttu-id="3ce2c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ce2c-112">-DefaultProfile</span></span>
<span data-ttu-id="3ce2c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ce2c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ce2c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ce2c-114">-Name</span></span>
<span data-ttu-id="3ce2c-115">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-115">Specifies the name of the account.</span></span>
<span data-ttu-id="3ce2c-116">Этот командлет получает ключи для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-116">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ce2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="3ce2c-118">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ce2c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ce2c-119">CommonParameters</span></span>
<span data-ttu-id="3ce2c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ce2c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ce2c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ce2c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ce2c-122">INPUTS</span></span>

### <span data-ttu-id="3ce2c-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="3ce2c-123">None</span></span>
<span data-ttu-id="3ce2c-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3ce2c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ce2c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ce2c-125">OUTPUTS</span></span>

### <span data-ttu-id="3ce2c-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3ce2c-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="3ce2c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ce2c-127">NOTES</span></span>

## <span data-ttu-id="3ce2c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ce2c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3ce2c-129">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="3ce2c-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


