---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: 4892e5e31c67725d15af7be015ca27bd450babd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006648"
---
# <span data-ttu-id="e6414-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="e6414-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="e6414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6414-102">SYNOPSIS</span></span>
<span data-ttu-id="e6414-103">Повторно сгенерирует ключ учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e6414-103">Regenerates an account key.</span></span>

## <span data-ttu-id="e6414-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6414-104">SYNTAX</span></span>

### <span data-ttu-id="e6414-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6414-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6414-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6414-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6414-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6414-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6414-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6414-108">DESCRIPTION</span></span>
<span data-ttu-id="e6414-109">Новый New-AzMapsAccountKey-клиент повторно сгенерирует ключ API для учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="e6414-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="e6414-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6414-110">EXAMPLES</span></span>

### <span data-ttu-id="e6414-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6414-111">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceGroupName MyResourceGroup -Name MyAccount -KeyName Primary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Primary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e6414-112">Повторно сгенерирует первичный ключ API для учетной записи MyAccount в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e6414-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="e6414-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6414-113">Example 2</span></span>
```powershell
PS C:\> New-AzMapsAccountKey -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount -KeyName Secondary

Confirm
Are you sure you want to perform this action?
Performing the operation "Regenerating Key Secondary for account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y

Id                                                                                                                                              PrimaryKey                                  SecondaryKey
--                                                                                                                                              ----------                                  ------------
/subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount ******************************************* *******************************************
```

<span data-ttu-id="e6414-114">Повторно сгенерирует ключ дополнительного API для указанной учетной записи Карты Azure.</span><span class="sxs-lookup"><span data-stu-id="e6414-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="e6414-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6414-115">PARAMETERS</span></span>

### <span data-ttu-id="e6414-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6414-116">-DefaultProfile</span></span>
<span data-ttu-id="e6414-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6414-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6414-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6414-118">-InputObject</span></span>
<span data-ttu-id="e6414-119">"Учетная запись Карты" в канале Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="e6414-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="e6414-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e6414-120">-KeyName</span></span>
<span data-ttu-id="e6414-121">"Карты" с ключом учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e6414-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="e6414-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e6414-122">-Name</span></span>
<span data-ttu-id="e6414-123">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="e6414-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="e6414-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6414-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6414-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6414-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e6414-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6414-126">-ResourceId</span></span>
<span data-ttu-id="e6414-127">Карты Account ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e6414-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="e6414-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6414-128">-Confirm</span></span>
<span data-ttu-id="e6414-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6414-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6414-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6414-130">-WhatIf</span></span>
<span data-ttu-id="e6414-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6414-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6414-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e6414-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6414-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6414-133">CommonParameters</span></span>
<span data-ttu-id="e6414-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6414-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6414-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6414-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6414-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6414-136">INPUTS</span></span>

### <span data-ttu-id="e6414-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e6414-137">System.String</span></span>

### <span data-ttu-id="e6414-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="e6414-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="e6414-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6414-139">OUTPUTS</span></span>

### <span data-ttu-id="e6414-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e6414-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="e6414-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6414-141">NOTES</span></span>

## <span data-ttu-id="e6414-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6414-142">RELATED LINKS</span></span>
