---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: 3f442cc975c6fdbb95d53153c2c80615bb8676a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246907"
---
# <span data-ttu-id="bcf47-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf47-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="bcf47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcf47-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf47-103">Возвращает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="bcf47-103">Gets an account.</span></span>

## <span data-ttu-id="bcf47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcf47-104">SYNTAX</span></span>

### <span data-ttu-id="bcf47-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf47-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf47-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcf47-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf47-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcf47-107">DESCRIPTION</span></span>
<span data-ttu-id="bcf47-108">Командлет **Get-AzCognitiveServicesAccount** получает учетные записи для предоставленных персонализированных служб в группе ресурсов, заданной параметром *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="bcf47-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="bcf47-109">Если параметр *ResourceGroupName* не указан, этот командлет получает все учетные записи для действующих служб для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="bcf47-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="bcf47-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcf47-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf47-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcf47-111">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locati
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

## <span data-ttu-id="bcf47-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcf47-112">PARAMETERS</span></span>

### <span data-ttu-id="bcf47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf47-113">-DefaultProfile</span></span>
<span data-ttu-id="bcf47-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bcf47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcf47-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcf47-115">-Name</span></span>
<span data-ttu-id="bcf47-116">Указывает имя учетной записи для восприятия служб, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bcf47-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="bcf47-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf47-117">-ResourceGroupName</span></span>
<span data-ttu-id="bcf47-118">Указывает имя группы ресурсов, которой назначена учетная запись службы.</span><span class="sxs-lookup"><span data-stu-id="bcf47-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="bcf47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf47-119">CommonParameters</span></span>
<span data-ttu-id="bcf47-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcf47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf47-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bcf47-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf47-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcf47-122">INPUTS</span></span>

### <span data-ttu-id="bcf47-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf47-123">System.String</span></span>

## <span data-ttu-id="bcf47-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcf47-124">OUTPUTS</span></span>

### <span data-ttu-id="bcf47-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf47-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="bcf47-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcf47-126">NOTES</span></span>

## <span data-ttu-id="bcf47-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcf47-127">RELATED LINKS</span></span>

[<span data-ttu-id="bcf47-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf47-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bcf47-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf47-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="bcf47-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="bcf47-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


