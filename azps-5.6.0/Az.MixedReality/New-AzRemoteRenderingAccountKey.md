---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: 8bfc07b5502c2dd648beea827af9587c9e6d9447
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970531"
---
# <span data-ttu-id="7a59e-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="7a59e-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="7a59e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a59e-102">SYNOPSIS</span></span>
<span data-ttu-id="7a59e-103">Повторное сгенерировать ключ учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="7a59e-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="7a59e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a59e-104">SYNTAX</span></span>

### <span data-ttu-id="7a59e-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a59e-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a59e-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a59e-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a59e-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a59e-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a59e-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a59e-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a59e-111">DESCRIPTION</span></span>
<span data-ttu-id="7a59e-112">Повторно сгенерировать первичный или дополнительный ключ учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7a59e-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="7a59e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a59e-113">EXAMPLES</span></span>

### <span data-ttu-id="7a59e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a59e-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="7a59e-115">Повторно сгенерировать дополнительный ключ "example" учетной записи удаленной отрисовки в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="7a59e-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="7a59e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7a59e-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="7a59e-117">Повторно сгенерировать дополнительный ключ "example" учетной записи удаленной отрисовки из текущей подписки и группы ресурсов "rg1" с помощью piping.</span><span class="sxs-lookup"><span data-stu-id="7a59e-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="7a59e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a59e-118">PARAMETERS</span></span>

### <span data-ttu-id="7a59e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a59e-119">-DefaultProfile</span></span>
<span data-ttu-id="7a59e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a59e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a59e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7a59e-121">-Force</span></span>
<span data-ttu-id="7a59e-122">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7a59e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7a59e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a59e-123">-InputObject</span></span>
<span data-ttu-id="7a59e-124">Объект настраиваемного домена.</span><span class="sxs-lookup"><span data-stu-id="7a59e-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7a59e-125">-Name</span></span>
<span data-ttu-id="7a59e-126">Имя учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7a59e-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="7a59e-127">-Primary</span></span>
<span data-ttu-id="7a59e-128">Повторно сгенерировать первичный ключ учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7a59e-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a59e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a59e-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a59e-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a59e-131">-ResourceId</span></span>
<span data-ttu-id="7a59e-132">ИД ресурса учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7a59e-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-133">-Secondary</span><span class="sxs-lookup"><span data-stu-id="7a59e-133">-Secondary</span></span>
<span data-ttu-id="7a59e-134">Повторно сгенерировать первичный ключ учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="7a59e-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a59e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a59e-135">-Confirm</span></span>
<span data-ttu-id="7a59e-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a59e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a59e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a59e-137">-WhatIf</span></span>
<span data-ttu-id="7a59e-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a59e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a59e-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a59e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a59e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a59e-140">CommonParameters</span></span>
<span data-ttu-id="7a59e-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a59e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7a59e-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a59e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a59e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a59e-143">INPUTS</span></span>

### <span data-ttu-id="7a59e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7a59e-144">System.String</span></span>

### <span data-ttu-id="7a59e-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7a59e-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="7a59e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a59e-146">OUTPUTS</span></span>

### <span data-ttu-id="7a59e-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7a59e-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="7a59e-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a59e-148">NOTES</span></span>

## <span data-ttu-id="7a59e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a59e-149">RELATED LINKS</span></span>
