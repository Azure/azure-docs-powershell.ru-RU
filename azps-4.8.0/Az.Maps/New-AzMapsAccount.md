---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079019"
---
# <span data-ttu-id="76a35-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="76a35-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="76a35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76a35-102">SYNOPSIS</span></span>
<span data-ttu-id="76a35-103">Создание учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="76a35-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="76a35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76a35-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a35-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a35-105">DESCRIPTION</span></span>
<span data-ttu-id="76a35-106">Командлет New-AzMapsAccount создает учетную запись карт Azure с указанным SKU.</span><span class="sxs-lookup"><span data-stu-id="76a35-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="76a35-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76a35-107">EXAMPLES</span></span>

### <span data-ttu-id="76a35-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="76a35-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="76a35-109">Создает новую учетную запись карт Azure с именем Моя учетная запись в группе ресурсов MyResourceGroup с помощью SKU S0 и тега.</span><span class="sxs-lookup"><span data-stu-id="76a35-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="76a35-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76a35-110">PARAMETERS</span></span>

### <span data-ttu-id="76a35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a35-111">-DefaultProfile</span></span>
<span data-ttu-id="76a35-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76a35-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a35-113">-Force</span><span class="sxs-lookup"><span data-stu-id="76a35-113">-Force</span></span>
<span data-ttu-id="76a35-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="76a35-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76a35-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76a35-115">-Name</span></span>
<span data-ttu-id="76a35-116">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="76a35-116">Maps Account Name.</span></span>

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

### <span data-ttu-id="76a35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a35-117">-ResourceGroupName</span></span>
<span data-ttu-id="76a35-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76a35-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="76a35-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="76a35-119">-SkuName</span></span>
<span data-ttu-id="76a35-120">Номер SKU учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="76a35-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76a35-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="76a35-121">-Tag</span></span>
<span data-ttu-id="76a35-122">Сопоставляет Теги учетной записи.</span><span class="sxs-lookup"><span data-stu-id="76a35-122">Maps Account Tags.</span></span>

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

### <span data-ttu-id="76a35-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76a35-123">-Confirm</span></span>
<span data-ttu-id="76a35-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76a35-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a35-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a35-125">-WhatIf</span></span>
<span data-ttu-id="76a35-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76a35-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a35-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76a35-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a35-128">CommonParameters</span></span>
<span data-ttu-id="76a35-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76a35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a35-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76a35-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a35-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76a35-131">INPUTS</span></span>

### <span data-ttu-id="76a35-132">System. String</span><span class="sxs-lookup"><span data-stu-id="76a35-132">System.String</span></span>

## <span data-ttu-id="76a35-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76a35-133">OUTPUTS</span></span>

### <span data-ttu-id="76a35-134">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="76a35-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="76a35-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="76a35-135">NOTES</span></span>

## <span data-ttu-id="76a35-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76a35-136">RELATED LINKS</span></span>
