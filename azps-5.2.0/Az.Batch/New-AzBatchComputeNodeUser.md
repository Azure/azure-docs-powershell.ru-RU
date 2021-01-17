---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 5695f0bf0a7cc65b1eb032be33116cc40ec0618e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327799"
---
# <span data-ttu-id="208a1-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="208a1-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="208a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="208a1-102">SYNOPSIS</span></span>
<span data-ttu-id="208a1-103">Создает учетную запись пользователя на узле пакетных вычислений.</span><span class="sxs-lookup"><span data-stu-id="208a1-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="208a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="208a1-104">SYNTAX</span></span>

### <span data-ttu-id="208a1-105">ИД</span><span class="sxs-lookup"><span data-stu-id="208a1-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="208a1-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="208a1-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="208a1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="208a1-107">DESCRIPTION</span></span>
<span data-ttu-id="208a1-108">Для создания учетной записи пользователя в узле обработки пакетных вычислений Azure создается учетная запись **new-AzBatchComputeNodeUser.**</span><span class="sxs-lookup"><span data-stu-id="208a1-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="208a1-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="208a1-109">EXAMPLES</span></span>

### <span data-ttu-id="208a1-110">Пример 1. Создание учетной записи пользователя с учетными данными администратора</span><span class="sxs-lookup"><span data-stu-id="208a1-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="208a1-111">Эта команда создает учетную запись пользователя на узле вычислений, который имеет ID ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="208a1-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="208a1-112">Узел находится в пуле с ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="208a1-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="208a1-113">Имя пользователя — TestUser, пароль — Password, срок действия учетной записи истекает через семь дней, а учетная запись имеет учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="208a1-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="208a1-114">Пример 2. Создание учетной записи пользователя на узле вычислений с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="208a1-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="208a1-115">Эта команда получает узел вычислений ComputeNode01 с помощью командлета **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="208a1-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="208a1-116">Этот узел находится в пуле с ID MyPool01.</span><span class="sxs-lookup"><span data-stu-id="208a1-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="208a1-117">Эта команда передает этот узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="208a1-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="208a1-118">Эта команда создает учетную запись пользователя с именем пользователя TestUser и паролем.</span><span class="sxs-lookup"><span data-stu-id="208a1-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="208a1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="208a1-119">PARAMETERS</span></span>

### <span data-ttu-id="208a1-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="208a1-120">-BatchContext</span></span>
<span data-ttu-id="208a1-121">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="208a1-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="208a1-122">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="208a1-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="208a1-123">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="208a1-123">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="208a1-124">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="208a1-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="208a1-125">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="208a1-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="208a1-126">-ComputeNode</span></span>
<span data-ttu-id="208a1-127">Определяет узел вычислений в качестве объекта **PSComputeNode,** на котором этот cmdlet создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="208a1-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="208a1-128">-ComputeNodeId</span></span>
<span data-ttu-id="208a1-129">Определяет код узла вычислений, на котором этот cmdlet создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="208a1-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="208a1-130">-DefaultProfile</span></span>
<span data-ttu-id="208a1-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="208a1-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="208a1-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="208a1-132">-ExpiryTime</span></span>
<span data-ttu-id="208a1-133">Указывает срок действия для новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="208a1-133">Specifies the expiry time for the new user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-134">-IsAdmin</span><span class="sxs-lookup"><span data-stu-id="208a1-134">-IsAdmin</span></span>
<span data-ttu-id="208a1-135">Указывает на то, что при этом создается учетная запись пользователя с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="208a1-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="208a1-136">-Name</span><span class="sxs-lookup"><span data-stu-id="208a1-136">-Name</span></span>
<span data-ttu-id="208a1-137">Указывает имя новой локальной учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="208a1-137">Specifies the name of the new local Windows account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-138">-Password</span><span class="sxs-lookup"><span data-stu-id="208a1-138">-Password</span></span>
<span data-ttu-id="208a1-139">Пароль учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="208a1-139">Specifies the user account password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="208a1-140">-PoolId</span></span>
<span data-ttu-id="208a1-141">Определяет ИД пула, который содержит узел вычислений, на котором нужно создать учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="208a1-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="208a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="208a1-142">CommonParameters</span></span>
<span data-ttu-id="208a1-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="208a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="208a1-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="208a1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="208a1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="208a1-145">INPUTS</span></span>

### <span data-ttu-id="208a1-146">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="208a1-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="208a1-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="208a1-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="208a1-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="208a1-148">OUTPUTS</span></span>

### <span data-ttu-id="208a1-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="208a1-149">System.Void</span></span>

## <span data-ttu-id="208a1-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="208a1-150">NOTES</span></span>

## <span data-ttu-id="208a1-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="208a1-151">RELATED LINKS</span></span>

[<span data-ttu-id="208a1-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="208a1-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="208a1-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="208a1-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="208a1-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="208a1-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="208a1-155">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="208a1-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
