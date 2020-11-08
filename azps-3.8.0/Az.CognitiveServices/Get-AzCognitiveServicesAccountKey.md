---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 8150abc726f990b699237dbaad3641a99bae2e2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064787"
---
# <span data-ttu-id="5bbf0-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5bbf0-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="5bbf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbf0-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="5bbf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bbf0-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bbf0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbf0-106">Командлет **Get-AzCognitiveServicesAccountKey** получает ключи API для учетной записи настроенных персонализированных служб.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="5bbf0-107">Учетная запись службы использует два ключа API: key1 и Key2.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="5bbf0-108">Ключи обеспечивают взаимодействие с конечной точкой учетной записи самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="5bbf0-109">Для повторного создания ключа используйте New-AzCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="5bbf0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-110">EXAMPLES</span></span>

### <span data-ttu-id="5bbf0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5bbf0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="5bbf0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-112">PARAMETERS</span></span>

### <span data-ttu-id="5bbf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bbf0-113">-DefaultProfile</span></span>
<span data-ttu-id="5bbf0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5bbf0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bbf0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5bbf0-115">-Name</span></span>
<span data-ttu-id="5bbf0-116">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-116">Specifies the name of the account.</span></span>
<span data-ttu-id="5bbf0-117">Этот командлет получает ключи для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="5bbf0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bbf0-118">-ResourceGroupName</span></span>
<span data-ttu-id="5bbf0-119">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="5bbf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbf0-120">CommonParameters</span></span>
<span data-ttu-id="5bbf0-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bbf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbf0-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bbf0-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbf0-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bbf0-123">INPUTS</span></span>

### <span data-ttu-id="5bbf0-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5bbf0-124">System.String</span></span>

## <span data-ttu-id="5bbf0-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-125">OUTPUTS</span></span>

### <span data-ttu-id="5bbf0-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5bbf0-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="5bbf0-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bbf0-127">NOTES</span></span>

## <span data-ttu-id="5bbf0-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bbf0-128">RELATED LINKS</span></span>

[<span data-ttu-id="5bbf0-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="5bbf0-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


