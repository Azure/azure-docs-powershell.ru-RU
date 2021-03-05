---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccount.md
ms.openlocfilehash: ccbba2c5fb6c417284ae025cf1410d68bb3c8add
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007160"
---
# <span data-ttu-id="47f83-101">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f83-101">Get-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="47f83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47f83-102">SYNOPSIS</span></span>
<span data-ttu-id="47f83-103">Получает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="47f83-103">Gets an account.</span></span>

## <span data-ttu-id="47f83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47f83-104">SYNTAX</span></span>

### <span data-ttu-id="47f83-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f83-105">ResourceGroupParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47f83-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47f83-106">AccountNameParameterSet</span></span>
```
Get-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47f83-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47f83-107">DESCRIPTION</span></span>
<span data-ttu-id="47f83-108">**Cmdlet Get-AzCognitiveServicesAccount** получает учетные записи provisioned Cognitive Services в группе ресурсов, задаемой параметром *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="47f83-108">The **Get-AzCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="47f83-109">Если параметр *ResourceGroupName* не задан, этот cmdlet возвращает все учетные записи службы когнитивных услуг для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="47f83-109">If you do not specify the *ResourceGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="47f83-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47f83-110">EXAMPLES</span></span>

### <span data-ttu-id="47f83-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47f83-111">Example 1</span></span>
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

## <span data-ttu-id="47f83-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47f83-112">PARAMETERS</span></span>

### <span data-ttu-id="47f83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47f83-113">-DefaultProfile</span></span>
<span data-ttu-id="47f83-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47f83-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47f83-115">-Name</span><span class="sxs-lookup"><span data-stu-id="47f83-115">-Name</span></span>
<span data-ttu-id="47f83-116">Указывает имя учетной записи "Когнитивные службы", которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="47f83-116">Specifies the name of the Cognitive Services account to get.</span></span>

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

### <span data-ttu-id="47f83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47f83-117">-ResourceGroupName</span></span>
<span data-ttu-id="47f83-118">Имя группы ресурсов, которая назначена учетной записи "Когнитивные услуги".</span><span class="sxs-lookup"><span data-stu-id="47f83-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="47f83-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47f83-119">CommonParameters</span></span>
<span data-ttu-id="47f83-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47f83-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47f83-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47f83-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47f83-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47f83-122">INPUTS</span></span>

### <span data-ttu-id="47f83-123">System.String</span><span class="sxs-lookup"><span data-stu-id="47f83-123">System.String</span></span>

## <span data-ttu-id="47f83-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47f83-124">OUTPUTS</span></span>

### <span data-ttu-id="47f83-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f83-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="47f83-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47f83-126">NOTES</span></span>

## <span data-ttu-id="47f83-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47f83-127">RELATED LINKS</span></span>

[<span data-ttu-id="47f83-128">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f83-128">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="47f83-129">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f83-129">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="47f83-130">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="47f83-130">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


