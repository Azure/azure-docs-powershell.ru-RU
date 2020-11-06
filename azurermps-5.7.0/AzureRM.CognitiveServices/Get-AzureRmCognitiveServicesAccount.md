---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565582"
---
# <span data-ttu-id="dc549-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dc549-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="dc549-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc549-102">SYNOPSIS</span></span>
<span data-ttu-id="dc549-103">Возвращает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="dc549-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc549-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc549-104">SYNTAX</span></span>

### <span data-ttu-id="dc549-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc549-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc549-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc549-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc549-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc549-107">DESCRIPTION</span></span>
<span data-ttu-id="dc549-108">Командлет **Get-AzureRmCognitiveServicesAccount** получает учетные записи для предоставленных персонализированных служб в группе ресурсов, заданной параметром *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="dc549-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="dc549-109">Если параметр *ResoureGroupName* не указан, этот командлет получает все учетные записи для действующих служб для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="dc549-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="dc549-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc549-110">EXAMPLES</span></span>

## <span data-ttu-id="dc549-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc549-111">PARAMETERS</span></span>

### <span data-ttu-id="dc549-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc549-112">-DefaultProfile</span></span>
<span data-ttu-id="dc549-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dc549-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc549-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc549-114">-Name</span></span>
<span data-ttu-id="dc549-115">Указывает имя учетной записи для восприятия служб, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="dc549-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc549-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc549-116">-ResourceGroupName</span></span>
<span data-ttu-id="dc549-117">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="dc549-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc549-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc549-118">CommonParameters</span></span>
<span data-ttu-id="dc549-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc549-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc549-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc549-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc549-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc549-121">INPUTS</span></span>

### <span data-ttu-id="dc549-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="dc549-122">None</span></span>
<span data-ttu-id="dc549-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="dc549-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dc549-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc549-124">OUTPUTS</span></span>

### <span data-ttu-id="dc549-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dc549-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="dc549-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc549-126">NOTES</span></span>

## <span data-ttu-id="dc549-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc549-127">RELATED LINKS</span></span>

[<span data-ttu-id="dc549-128">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dc549-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dc549-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dc549-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="dc549-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="dc549-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


