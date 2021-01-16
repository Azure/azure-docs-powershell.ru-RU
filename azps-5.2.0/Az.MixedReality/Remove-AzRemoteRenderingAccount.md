---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397431"
---
# <span data-ttu-id="aacbb-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="aacbb-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="aacbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aacbb-102">SYNOPSIS</span></span>
<span data-ttu-id="aacbb-103">Удаление учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="aacbb-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="aacbb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aacbb-104">SYNTAX</span></span>

### <span data-ttu-id="aacbb-105">DefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aacbb-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aacbb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aacbb-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aacbb-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="aacbb-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aacbb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aacbb-108">DESCRIPTION</span></span>
<span data-ttu-id="aacbb-109">Удаление указанной учетной записи удаленной отрисовки из определенной группы подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aacbb-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="aacbb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aacbb-110">EXAMPLES</span></span>

### <span data-ttu-id="aacbb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aacbb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="aacbb-112">Удалите "пример" удаленной учетной записи отрисовки из текущей подписки и группы ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="aacbb-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="aacbb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aacbb-113">PARAMETERS</span></span>

### <span data-ttu-id="aacbb-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aacbb-114">-Confirm</span></span>
<span data-ttu-id="aacbb-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="aacbb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aacbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aacbb-116">-DefaultProfile</span></span>
<span data-ttu-id="aacbb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aacbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aacbb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aacbb-118">-InputObject</span></span>
<span data-ttu-id="aacbb-119">Объект пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="aacbb-119">The custom domain object.</span></span>

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

### <span data-ttu-id="aacbb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="aacbb-120">-Name</span></span>
<span data-ttu-id="aacbb-121">Имя учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="aacbb-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="aacbb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aacbb-122">-PassThru</span></span>
<span data-ttu-id="aacbb-123">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="aacbb-123">Return object if specified.</span></span>

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

### <span data-ttu-id="aacbb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aacbb-124">-ResourceGroupName</span></span>
<span data-ttu-id="aacbb-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aacbb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="aacbb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aacbb-126">-ResourceId</span></span>
<span data-ttu-id="aacbb-127">ИД ресурса учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="aacbb-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="aacbb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aacbb-128">-WhatIf</span></span>
<span data-ttu-id="aacbb-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aacbb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aacbb-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aacbb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aacbb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aacbb-131">CommonParameters</span></span>
<span data-ttu-id="aacbb-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aacbb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="aacbb-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aacbb-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aacbb-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aacbb-134">INPUTS</span></span>

### <span data-ttu-id="aacbb-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aacbb-135">System.String</span></span>

### <span data-ttu-id="aacbb-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="aacbb-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="aacbb-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aacbb-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aacbb-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aacbb-138">OUTPUTS</span></span>

### <span data-ttu-id="aacbb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aacbb-139">System.Boolean</span></span>

## <span data-ttu-id="aacbb-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aacbb-140">NOTES</span></span>

## <span data-ttu-id="aacbb-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aacbb-141">RELATED LINKS</span></span>