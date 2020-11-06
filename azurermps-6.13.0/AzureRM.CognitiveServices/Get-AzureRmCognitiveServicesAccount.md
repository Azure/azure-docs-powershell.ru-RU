---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 3f139d4164c092f6ef57ad29d5ab9ad3eac59b56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567292"
---
# <span data-ttu-id="826c7-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="826c7-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="826c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="826c7-102">SYNOPSIS</span></span>
<span data-ttu-id="826c7-103">Возвращает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="826c7-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="826c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="826c7-104">SYNTAX</span></span>

### <span data-ttu-id="826c7-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="826c7-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="826c7-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="826c7-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="826c7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="826c7-107">DESCRIPTION</span></span>
<span data-ttu-id="826c7-108">Командлет **Get-AzureRmCognitiveServicesAccount** получает учетные записи для предоставленных персонализированных служб в группе ресурсов, заданной параметром *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="826c7-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>
<span data-ttu-id="826c7-109">Если параметр *ResoureGroupName* не указан, этот командлет получает все учетные записи для действующих служб для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="826c7-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="826c7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="826c7-110">EXAMPLES</span></span>

### <span data-ttu-id="826c7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="826c7-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
on 'WestUS'

ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="826c7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="826c7-112">PARAMETERS</span></span>

### <span data-ttu-id="826c7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="826c7-113">-DefaultProfile</span></span>
<span data-ttu-id="826c7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="826c7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="826c7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="826c7-115">-Name</span></span>
<span data-ttu-id="826c7-116">Указывает имя учетной записи для восприятия служб, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="826c7-116">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826c7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="826c7-117">-ResourceGroupName</span></span>
<span data-ttu-id="826c7-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="826c7-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="826c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="826c7-119">CommonParameters</span></span>
<span data-ttu-id="826c7-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="826c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="826c7-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="826c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="826c7-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="826c7-122">INPUTS</span></span>

### <span data-ttu-id="826c7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="826c7-123">System.String</span></span>

## <span data-ttu-id="826c7-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="826c7-124">OUTPUTS</span></span>

### <span data-ttu-id="826c7-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="826c7-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="826c7-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="826c7-126">NOTES</span></span>

## <span data-ttu-id="826c7-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="826c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="826c7-128">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="826c7-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="826c7-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="826c7-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="826c7-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="826c7-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


