---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247310"
---
# <span data-ttu-id="30d25-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="30d25-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="30d25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30d25-102">SYNOPSIS</span></span>
<span data-ttu-id="30d25-103">Повторное создание ключа учетной записи удаленной отрисовки</span><span class="sxs-lookup"><span data-stu-id="30d25-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="30d25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30d25-104">SYNTAX</span></span>

### <span data-ttu-id="30d25-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d25-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d25-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d25-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d25-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30d25-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="30d25-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30d25-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30d25-111">DESCRIPTION</span></span>
<span data-ttu-id="30d25-112">Повторное создание первичного ключа или вторичного ключа учетной записи удаленной подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="30d25-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="30d25-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30d25-113">EXAMPLES</span></span>

### <span data-ttu-id="30d25-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="30d25-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="30d25-115">Повторное создание вторичного ключа учетной записи удаленной отрисовки "пример" в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="30d25-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="30d25-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="30d25-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="30d25-117">Повторное создание вторичного ключа учетной записи удаленной подготовки к просмотру "пример" из текущей подписки и группы ресурсов "Rg1" с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="30d25-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="30d25-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30d25-118">PARAMETERS</span></span>

### <span data-ttu-id="30d25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d25-119">-DefaultProfile</span></span>
<span data-ttu-id="30d25-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30d25-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30d25-121">-Force</span><span class="sxs-lookup"><span data-stu-id="30d25-121">-Force</span></span>
<span data-ttu-id="30d25-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="30d25-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30d25-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30d25-123">-InputObject</span></span>
<span data-ttu-id="30d25-124">Настраиваемый объект домена.</span><span class="sxs-lookup"><span data-stu-id="30d25-124">The custom domain object.</span></span>

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

### <span data-ttu-id="30d25-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="30d25-125">-Name</span></span>
<span data-ttu-id="30d25-126">Имя учетной записи для удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="30d25-126">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="30d25-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="30d25-127">-Primary</span></span>
<span data-ttu-id="30d25-128">Повторное создание первичного ключа учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="30d25-128">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="30d25-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30d25-129">-ResourceGroupName</span></span>
<span data-ttu-id="30d25-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="30d25-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="30d25-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30d25-131">-ResourceId</span></span>
<span data-ttu-id="30d25-132">Идентификатор ресурса для учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="30d25-132">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="30d25-133">-Получатель</span><span class="sxs-lookup"><span data-stu-id="30d25-133">-Secondary</span></span>
<span data-ttu-id="30d25-134">Повторное создание первичного ключа учетной записи удаленной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="30d25-134">Regenerate primary key of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="30d25-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30d25-135">-Confirm</span></span>
<span data-ttu-id="30d25-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="30d25-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30d25-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30d25-137">-WhatIf</span></span>
<span data-ttu-id="30d25-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="30d25-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30d25-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="30d25-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30d25-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d25-140">CommonParameters</span></span>
<span data-ttu-id="30d25-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30d25-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="30d25-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30d25-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d25-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30d25-143">INPUTS</span></span>

### <span data-ttu-id="30d25-144">System. String</span><span class="sxs-lookup"><span data-stu-id="30d25-144">System.String</span></span>

### <span data-ttu-id="30d25-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="30d25-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="30d25-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30d25-146">OUTPUTS</span></span>

### <span data-ttu-id="30d25-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="30d25-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="30d25-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="30d25-148">NOTES</span></span>

## <span data-ttu-id="30d25-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30d25-149">RELATED LINKS</span></span>
