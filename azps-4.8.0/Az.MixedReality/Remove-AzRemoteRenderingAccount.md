---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079931"
---
# <span data-ttu-id="51833-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="51833-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="51833-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51833-102">SYNOPSIS</span></span>
<span data-ttu-id="51833-103">Удаление учетной записи удаленной подготовки к просмотру</span><span class="sxs-lookup"><span data-stu-id="51833-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="51833-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51833-104">SYNTAX</span></span>

### <span data-ttu-id="51833-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51833-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51833-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51833-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51833-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="51833-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51833-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51833-108">DESCRIPTION</span></span>
<span data-ttu-id="51833-109">Удаление указанной учетной записи удаленной отрисовки из определенной подписки и группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51833-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="51833-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51833-110">EXAMPLES</span></span>

### <span data-ttu-id="51833-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="51833-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="51833-112">Удалить учетную запись удаленной отрисовки "пример" из текущей подписки и группы ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="51833-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="51833-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51833-113">PARAMETERS</span></span>

### <span data-ttu-id="51833-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51833-114">-Confirm</span></span>
<span data-ttu-id="51833-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51833-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51833-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51833-116">-DefaultProfile</span></span>
<span data-ttu-id="51833-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51833-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51833-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51833-118">-InputObject</span></span>
<span data-ttu-id="51833-119">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="51833-119">The custom domain object.</span></span>

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

### <span data-ttu-id="51833-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51833-120">-Name</span></span>
<span data-ttu-id="51833-121">Имя учетной записи для удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="51833-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="51833-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51833-122">-PassThru</span></span>
<span data-ttu-id="51833-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="51833-123">Return object if specified.</span></span>

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

### <span data-ttu-id="51833-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51833-124">-ResourceGroupName</span></span>
<span data-ttu-id="51833-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51833-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="51833-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51833-126">-ResourceId</span></span>
<span data-ttu-id="51833-127">Идентификатор ресурса для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="51833-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="51833-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51833-128">-WhatIf</span></span>
<span data-ttu-id="51833-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51833-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51833-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51833-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51833-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51833-131">CommonParameters</span></span>
<span data-ttu-id="51833-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51833-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="51833-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51833-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51833-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51833-134">INPUTS</span></span>

### <span data-ttu-id="51833-135">System. String</span><span class="sxs-lookup"><span data-stu-id="51833-135">System.String</span></span>

### <span data-ttu-id="51833-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="51833-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="51833-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="51833-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="51833-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51833-138">OUTPUTS</span></span>

### <span data-ttu-id="51833-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51833-139">System.Boolean</span></span>

## <span data-ttu-id="51833-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="51833-140">NOTES</span></span>

## <span data-ttu-id="51833-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51833-141">RELATED LINKS</span></span>
