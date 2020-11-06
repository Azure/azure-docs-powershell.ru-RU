---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560140"
---
# <span data-ttu-id="cfeb1-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="cfeb1-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="cfeb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfeb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cfeb1-103">Удаление учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfeb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfeb1-104">SYNTAX</span></span>

### <span data-ttu-id="cfeb1-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfeb1-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfeb1-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeb1-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfeb1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfeb1-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfeb1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfeb1-108">DESCRIPTION</span></span>
<span data-ttu-id="cfeb1-109">Командлет Remove-AzureRmMapsAccount удаляет указанную учетную запись карт Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="cfeb1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfeb1-110">EXAMPLES</span></span>

### <span data-ttu-id="cfeb1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfeb1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="cfeb1-112">Удаление учетной записи Моя учетная запись из группы ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="cfeb1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cfeb1-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="cfeb1-114">Удаляет указанную учетную запись карт Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="cfeb1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfeb1-115">PARAMETERS</span></span>

### <span data-ttu-id="cfeb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfeb1-116">-DefaultProfile</span></span>
<span data-ttu-id="cfeb1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfeb1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfeb1-118">-InputObject</span></span>
<span data-ttu-id="cfeb1-119">Карты сопоставляются с учетной записью Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

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

### <span data-ttu-id="cfeb1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfeb1-120">-Name</span></span>
<span data-ttu-id="cfeb1-121">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="cfeb1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfeb1-122">-PassThru</span></span>
<span data-ttu-id="cfeb1-123">Возвращает данные о том, успешно ли удалена указанная учетная запись.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="cfeb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfeb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="cfeb1-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="cfeb1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfeb1-126">-ResourceId</span></span>
<span data-ttu-id="cfeb1-127">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="cfeb1-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfeb1-128">-Confirm</span></span>
<span data-ttu-id="cfeb1-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfeb1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfeb1-130">-WhatIf</span></span>
<span data-ttu-id="cfeb1-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfeb1-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfeb1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfeb1-133">CommonParameters</span></span>
<span data-ttu-id="cfeb1-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfeb1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfeb1-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfeb1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfeb1-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfeb1-136">INPUTS</span></span>

### <span data-ttu-id="cfeb1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cfeb1-137">System.String</span></span>

### <span data-ttu-id="cfeb1-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="cfeb1-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="cfeb1-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cfeb1-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cfeb1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfeb1-140">OUTPUTS</span></span>

### <span data-ttu-id="cfeb1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cfeb1-141">System.Boolean</span></span>

## <span data-ttu-id="cfeb1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfeb1-142">NOTES</span></span>

## <span data-ttu-id="cfeb1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfeb1-143">RELATED LINKS</span></span>
