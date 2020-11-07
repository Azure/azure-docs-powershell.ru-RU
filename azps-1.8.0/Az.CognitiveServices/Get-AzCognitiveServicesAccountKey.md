---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 11285a805444c270740d7158f66aa538fecfa1b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731391"
---
# <span data-ttu-id="62709-101">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="62709-101">Get-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="62709-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62709-102">SYNOPSIS</span></span>
<span data-ttu-id="62709-103">Возвращает ключи API для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="62709-103">Gets the API keys for an account.</span></span>

## <span data-ttu-id="62709-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62709-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62709-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62709-105">DESCRIPTION</span></span>
<span data-ttu-id="62709-106">Командлет **Get-AzCognitiveServicesAccountKey** получает ключи API для учетной записи настроенных персонализированных служб.</span><span class="sxs-lookup"><span data-stu-id="62709-106">The **Get-AzCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="62709-107">Учетная запись службы использует два ключа API: key1 и Key2.</span><span class="sxs-lookup"><span data-stu-id="62709-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="62709-108">Ключи обеспечивают взаимодействие с конечной точкой учетной записи самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="62709-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="62709-109">Для повторного создания ключа используйте New-AzCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="62709-109">Use New-AzCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="62709-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62709-110">EXAMPLES</span></span>

### <span data-ttu-id="62709-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62709-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="62709-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62709-112">PARAMETERS</span></span>

### <span data-ttu-id="62709-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62709-113">-DefaultProfile</span></span>
<span data-ttu-id="62709-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="62709-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62709-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62709-115">-Name</span></span>
<span data-ttu-id="62709-116">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="62709-116">Specifies the name of the account.</span></span>
<span data-ttu-id="62709-117">Этот командлет получает ключи для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="62709-117">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="62709-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62709-118">-ResourceGroupName</span></span>
<span data-ttu-id="62709-119">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="62709-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="62709-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62709-120">CommonParameters</span></span>
<span data-ttu-id="62709-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62709-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62709-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62709-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62709-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62709-123">INPUTS</span></span>

### <span data-ttu-id="62709-124">System. String</span><span class="sxs-lookup"><span data-stu-id="62709-124">System.String</span></span>

## <span data-ttu-id="62709-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62709-125">OUTPUTS</span></span>

### <span data-ttu-id="62709-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="62709-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="62709-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="62709-127">NOTES</span></span>

## <span data-ttu-id="62709-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62709-128">RELATED LINKS</span></span>

[<span data-ttu-id="62709-129">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="62709-129">New-AzCognitiveServicesAccountKey</span></span>](./New-AzCognitiveServicesAccountKey.md)


