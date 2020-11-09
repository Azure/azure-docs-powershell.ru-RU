---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccountKey.md
ms.openlocfilehash: c115cd780750770e05bc55b1f70a7cfe33967fff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250102"
---
# <span data-ttu-id="8dbc2-101">New-AzMapsAccountKey</span><span class="sxs-lookup"><span data-stu-id="8dbc2-101">New-AzMapsAccountKey</span></span>

## <span data-ttu-id="8dbc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dbc2-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbc2-103">Повторное создание ключа учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-103">Regenerates an account key.</span></span>

## <span data-ttu-id="8dbc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dbc2-104">SYNTAX</span></span>

### <span data-ttu-id="8dbc2-105">NameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dbc2-105">NameParameterSet (Default)</span></span>
```
New-AzMapsAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbc2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbc2-106">InputObjectParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-InputObject <PSMapsAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbc2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbc2-107">ResourceIdParameterSet</span></span>
```
New-AzMapsAccountKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbc2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dbc2-108">DESCRIPTION</span></span>
<span data-ttu-id="8dbc2-109">Командлет New-AzMapsAccountKey повторно создает ключ API для учетной записи карт Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-109">The New-AzMapsAccountKey cmdlet regenerates an API key for a Azure Maps account.</span></span>

## <span data-ttu-id="8dbc2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dbc2-110">EXAMPLES</span></span>

### <span data-ttu-id="8dbc2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dbc2-111">Example 1</span></span>
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

<span data-ttu-id="8dbc2-112">Повторно создает основной ключ API для учетной записи Моя учетная запись в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-112">Regenerates the Primary API Key for the account MyAccount in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="8dbc2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8dbc2-113">Example 2</span></span>
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

<span data-ttu-id="8dbc2-114">Повторно создает вторичный ключ API для указанной учетной записи Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-114">Regenerates the Secondary API Key for the specified Azure Maps Account.</span></span>

## <span data-ttu-id="8dbc2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dbc2-115">PARAMETERS</span></span>

### <span data-ttu-id="8dbc2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbc2-116">-DefaultProfile</span></span>
<span data-ttu-id="8dbc2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dbc2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbc2-118">-InputObject</span></span>
<span data-ttu-id="8dbc2-119">Карты сопоставляются с учетной записью Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="8dbc2-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8dbc2-120">-KeyName</span></span>
<span data-ttu-id="8dbc2-121">Ключ учетной записи карт.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-121">Maps Account Key.</span></span>

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

### <span data-ttu-id="8dbc2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dbc2-122">-Name</span></span>
<span data-ttu-id="8dbc2-123">Имя учетной записи карты.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="8dbc2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbc2-124">-ResourceGroupName</span></span>
<span data-ttu-id="8dbc2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dbc2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbc2-126">-ResourceId</span></span>
<span data-ttu-id="8dbc2-127">Карта ResourceId для счета.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="8dbc2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dbc2-128">-Confirm</span></span>
<span data-ttu-id="8dbc2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbc2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbc2-130">-WhatIf</span></span>
<span data-ttu-id="8dbc2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbc2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbc2-133">CommonParameters</span></span>
<span data-ttu-id="8dbc2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dbc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbc2-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dbc2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbc2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dbc2-136">INPUTS</span></span>

### <span data-ttu-id="8dbc2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8dbc2-137">System.String</span></span>

### <span data-ttu-id="8dbc2-138">Microsoft. Azure. Commands. Maps. Models. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8dbc2-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="8dbc2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dbc2-139">OUTPUTS</span></span>

### <span data-ttu-id="8dbc2-140">Microsoft. Azure. Management. Maps. Models. MapsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8dbc2-140">Microsoft.Azure.Management.Maps.Models.MapsAccountKeys</span></span>

## <span data-ttu-id="8dbc2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dbc2-141">NOTES</span></span>

## <span data-ttu-id="8dbc2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dbc2-142">RELATED LINKS</span></span>