---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2544531d9a988daaea314fc2088609df77b719b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731387"
---
# <span data-ttu-id="5511d-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5511d-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="5511d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5511d-102">SYNOPSIS</span></span>
<span data-ttu-id="5511d-103">Изменение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5511d-103">Modifies an account.</span></span>

## <span data-ttu-id="5511d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5511d-104">SYNTAX</span></span>

```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5511d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5511d-105">DESCRIPTION</span></span>
<span data-ttu-id="5511d-106">Командлет **Set-AzCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="5511d-106">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="5511d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5511d-107">EXAMPLES</span></span>

### <span data-ttu-id="5511d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5511d-108">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


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

## <span data-ttu-id="5511d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5511d-109">PARAMETERS</span></span>

### <span data-ttu-id="5511d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5511d-110">-DefaultProfile</span></span>
<span data-ttu-id="5511d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5511d-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5511d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="5511d-112">-Force</span></span>
<span data-ttu-id="5511d-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5511d-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5511d-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5511d-114">-Name</span></span>
<span data-ttu-id="5511d-115">Указывает имя учетной записи, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5511d-115">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="5511d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5511d-116">-ResourceGroupName</span></span>
<span data-ttu-id="5511d-117">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="5511d-117">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="5511d-118">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5511d-118">-SkuName</span></span>
<span data-ttu-id="5511d-119">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5511d-119">Specifies the SKU for the account.</span></span>
<span data-ttu-id="5511d-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5511d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5511d-121">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="5511d-121">F0 (free tier)</span></span>
- <span data-ttu-id="5511d-122">S0</span><span class="sxs-lookup"><span data-stu-id="5511d-122">S0</span></span>
- <span data-ttu-id="5511d-123">Состояний</span><span class="sxs-lookup"><span data-stu-id="5511d-123">S1</span></span>
- <span data-ttu-id="5511d-124">S2</span><span class="sxs-lookup"><span data-stu-id="5511d-124">S2</span></span>
- <span data-ttu-id="5511d-125">Режима</span><span class="sxs-lookup"><span data-stu-id="5511d-125">S3</span></span>
- <span data-ttu-id="5511d-126">Режим</span><span class="sxs-lookup"><span data-stu-id="5511d-126">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5511d-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="5511d-127">-Tag</span></span>
<span data-ttu-id="5511d-128">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="5511d-128">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5511d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5511d-129">-Confirm</span></span>
<span data-ttu-id="5511d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5511d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5511d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5511d-131">-WhatIf</span></span>
<span data-ttu-id="5511d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5511d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5511d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5511d-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5511d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5511d-134">CommonParameters</span></span>
<span data-ttu-id="5511d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5511d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5511d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5511d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5511d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5511d-137">INPUTS</span></span>

### <span data-ttu-id="5511d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5511d-138">System.String</span></span>

### <span data-ttu-id="5511d-139">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="5511d-139">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="5511d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5511d-140">OUTPUTS</span></span>

### <span data-ttu-id="5511d-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5511d-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="5511d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5511d-142">NOTES</span></span>

## <span data-ttu-id="5511d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5511d-143">RELATED LINKS</span></span>

[<span data-ttu-id="5511d-144">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5511d-144">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="5511d-145">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5511d-145">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="5511d-146">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="5511d-146">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
