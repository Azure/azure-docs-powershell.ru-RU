---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/new-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/New-AzureRmMapsAccount.md
ms.openlocfilehash: 0b8bfad1b3bb9f24c6b7c74e92f64c64d776c2d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565381"
---
# <span data-ttu-id="dee5a-101">New-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="dee5a-101">New-AzureRmMapsAccount</span></span>

## <span data-ttu-id="dee5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dee5a-102">SYNOPSIS</span></span>
<span data-ttu-id="dee5a-103">Создание учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="dee5a-103">Creates an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dee5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dee5a-104">SYNTAX</span></span>

```
New-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dee5a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee5a-105">DESCRIPTION</span></span>
<span data-ttu-id="dee5a-106">Командлет New-AzureRmMapsAccount создает учетную запись карт Azure с указанным SKU.</span><span class="sxs-lookup"><span data-stu-id="dee5a-106">The New-AzureRmMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="dee5a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dee5a-107">EXAMPLES</span></span>

### <span data-ttu-id="dee5a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dee5a-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="dee5a-109">Создает новую учетную запись карт Azure с именем Моя учетная запись в группе ресурсов MyResourceGroup с помощью SKU S0 и тега.</span><span class="sxs-lookup"><span data-stu-id="dee5a-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="dee5a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dee5a-110">PARAMETERS</span></span>

### <span data-ttu-id="dee5a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee5a-111">-DefaultProfile</span></span>
<span data-ttu-id="dee5a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dee5a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee5a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dee5a-113">-Force</span></span>
<span data-ttu-id="dee5a-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="dee5a-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dee5a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dee5a-115">-Name</span></span>
<span data-ttu-id="dee5a-116">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="dee5a-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee5a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee5a-117">-ResourceGroupName</span></span>
<span data-ttu-id="dee5a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dee5a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="dee5a-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dee5a-119">-SkuName</span></span>
<span data-ttu-id="dee5a-120">Номер SKU учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="dee5a-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee5a-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="dee5a-121">-Tag</span></span>
<span data-ttu-id="dee5a-122">Сопоставляет Теги учетной записи.</span><span class="sxs-lookup"><span data-stu-id="dee5a-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee5a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dee5a-123">-Confirm</span></span>
<span data-ttu-id="dee5a-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dee5a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dee5a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee5a-125">-WhatIf</span></span>
<span data-ttu-id="dee5a-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dee5a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dee5a-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dee5a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dee5a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee5a-128">CommonParameters</span></span>
<span data-ttu-id="dee5a-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dee5a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee5a-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dee5a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee5a-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dee5a-131">INPUTS</span></span>

### <span data-ttu-id="dee5a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dee5a-132">System.String</span></span>

## <span data-ttu-id="dee5a-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dee5a-133">OUTPUTS</span></span>

### <span data-ttu-id="dee5a-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="dee5a-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="dee5a-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="dee5a-135">NOTES</span></span>

## <span data-ttu-id="dee5a-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dee5a-136">RELATED LINKS</span></span>
