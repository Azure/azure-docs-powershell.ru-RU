---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247300"
---
# <span data-ttu-id="6ac1f-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="6ac1f-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="6ac1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ac1f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac1f-103">Удаление учетной записи удаленной подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="6ac1f-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="6ac1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ac1f-104">SYNTAX</span></span>

### <span data-ttu-id="6ac1f-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ac1f-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ac1f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ac1f-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ac1f-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ac1f-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac1f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ac1f-108">DESCRIPTION</span></span>
<span data-ttu-id="6ac1f-109">Удаление указанной учетной записи удаленной отрисовки из определенной подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="6ac1f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ac1f-110">EXAMPLES</span></span>

### <span data-ttu-id="6ac1f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ac1f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="6ac1f-112">Удалить учетную запись удаленной отрисовки "пример" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="6ac1f-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="6ac1f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ac1f-113">PARAMETERS</span></span>

### <span data-ttu-id="6ac1f-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ac1f-114">-Confirm</span></span>
<span data-ttu-id="6ac1f-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac1f-116">-DefaultProfile</span></span>
<span data-ttu-id="6ac1f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ac1f-118">-InputObject</span></span>
<span data-ttu-id="6ac1f-119">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6ac1f-120">-Name</span></span>
<span data-ttu-id="6ac1f-121">Имя учетной записи для удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ac1f-122">-PassThru</span></span>
<span data-ttu-id="6ac1f-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac1f-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ac1f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ac1f-126">-ResourceId</span></span>
<span data-ttu-id="6ac1f-127">Идентификатор ресурса для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac1f-128">-WhatIf</span></span>
<span data-ttu-id="6ac1f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac1f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ac1f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac1f-131">CommonParameters</span></span>
<span data-ttu-id="6ac1f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ac1f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6ac1f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac1f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac1f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ac1f-134">INPUTS</span></span>

### <span data-ttu-id="6ac1f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6ac1f-135">System.String</span></span>

### <span data-ttu-id="6ac1f-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="6ac1f-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="6ac1f-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6ac1f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6ac1f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ac1f-138">OUTPUTS</span></span>

### <span data-ttu-id="6ac1f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ac1f-139">System.Boolean</span></span>

## <span data-ttu-id="6ac1f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ac1f-140">NOTES</span></span>

## <span data-ttu-id="6ac1f-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ac1f-141">RELATED LINKS</span></span>
