---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccountKey.md
ms.openlocfilehash: 13364cde6799a6d99bcdba1d5cd2078c3392a2cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565379"
---
# <span data-ttu-id="ebc06-101">New-AzureRmMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ebc06-101">New-AzureRmMapsAccountKey</span></span>

## <span data-ttu-id="ebc06-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebc06-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc06-103">Повторное создание ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ebc06-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebc06-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebc06-104">SYNTAX</span></span>

### <span data-ttu-id="ebc06-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebc06-105">NameParameterSet (Default)</span></span>
```
New-AzureRmMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc06-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc06-106">InputObjectParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebc06-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc06-107">ResourceIdParameterSet</span></span>
```
New-AzureRmMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebc06-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebc06-108">DESCRIPTION</span></span>
<span data-ttu-id="ebc06-109">Командлет New-AzureRmMapsAccountKey повторно создает ключ API для учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc06-109">The New-AzureRmMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="ebc06-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebc06-110">EXAMPLES</span></span>

### <span data-ttu-id="ebc06-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebc06-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="ebc06-112">Повторно создает основной ключ API для учетной записи Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ebc06-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="ebc06-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ebc06-113">Example 2</span></span>
```powershell
PS C:\> New-AzureRmMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="ebc06-114">Повторно создает вторичный ключ API для указанной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="ebc06-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="ebc06-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebc06-115">PARAMETERS</span></span>

### <span data-ttu-id="ebc06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc06-116">-DefaultProfile</span></span>
<span data-ttu-id="ebc06-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebc06-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebc06-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebc06-118">-InputObject</span></span>
<span data-ttu-id="ebc06-119">Карты сопоставляются с учетной записью Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="ebc06-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ebc06-120">-KeyName</span></span>
<span data-ttu-id="ebc06-121">Ключ учетной записи карт.</span><span class="sxs-lookup"><span data-stu-id="ebc06-121">Maps Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ebc06-122">-Name</span></span>
<span data-ttu-id="ebc06-123">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="ebc06-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc06-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebc06-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ebc06-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebc06-126">-ResourceId</span></span>
<span data-ttu-id="ebc06-127">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="ebc06-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebc06-128">-Confirm</span></span>
<span data-ttu-id="ebc06-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ebc06-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebc06-130">-WhatIf</span></span>
<span data-ttu-id="ebc06-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ebc06-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebc06-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ebc06-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebc06-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc06-133">CommonParameters</span></span>
<span data-ttu-id="ebc06-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebc06-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc06-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc06-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc06-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebc06-136">INPUTS</span></span>

### <span data-ttu-id="ebc06-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ebc06-137">System.String</span></span>

### <span data-ttu-id="ebc06-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="ebc06-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="ebc06-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ebc06-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ebc06-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebc06-140">OUTPUTS</span></span>

### <span data-ttu-id="ebc06-141">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ebc06-141">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="ebc06-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebc06-142">NOTES</span></span>

## <span data-ttu-id="ebc06-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebc06-143">RELATED LINKS</span></span>
