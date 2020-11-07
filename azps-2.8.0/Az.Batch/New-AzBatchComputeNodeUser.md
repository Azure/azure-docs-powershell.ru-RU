---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchComputeNodeUser.md
ms.openlocfilehash: 415026112828685a053dd8ec37cb0042f0114af3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913222"
---
# <span data-ttu-id="cc517-101">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cc517-101">New-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="cc517-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc517-102">SYNOPSIS</span></span>
<span data-ttu-id="cc517-103">Создание учетной записи пользователя на пакетном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="cc517-103">Creates a user account on a Batch compute node.</span></span>

## <span data-ttu-id="cc517-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc517-104">SYNTAX</span></span>

### <span data-ttu-id="cc517-105">Номер</span><span class="sxs-lookup"><span data-stu-id="cc517-105">Id</span></span>
```
New-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc517-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="cc517-106">ParentObject</span></span>
```
New-AzBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc517-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc517-107">DESCRIPTION</span></span>
<span data-ttu-id="cc517-108">Командлет **New-AzBatchComputeNodeUser** создает учетную запись пользователя на пакетном кластере Azure.</span><span class="sxs-lookup"><span data-stu-id="cc517-108">The **New-AzBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="cc517-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc517-109">EXAMPLES</span></span>

### <span data-ttu-id="cc517-110">Пример 1: создание учетной записи пользователя с правами администратора</span><span class="sxs-lookup"><span data-stu-id="cc517-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="cc517-111">Эта команда создает учетную запись пользователя на узле COMPUTE node с ИД ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="cc517-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="cc517-112">Узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="cc517-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="cc517-113">Имя пользователя: TestUser, пароль — это пароль, срок действия учетной записи истекает через семь дней, а учетная запись имеет учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="cc517-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="cc517-114">Пример 2: создание учетной записи пользователя на вычислительном узле с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="cc517-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="cc517-115">Эта команда получает узел COMPUTE node с именем ComputeNode01 с помощью командлета **Get-AzBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="cc517-115">This command gets the compute node named ComputeNode01 by using the **Get-AzBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="cc517-116">Этот узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="cc517-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="cc517-117">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="cc517-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cc517-118">Эта команда создает учетную запись пользователя с именем пользователя и паролем пароля.</span><span class="sxs-lookup"><span data-stu-id="cc517-118">The command creates a user account that has the user name TestUser and the password Password.</span></span>

## <span data-ttu-id="cc517-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc517-119">PARAMETERS</span></span>

### <span data-ttu-id="cc517-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="cc517-120">-BatchContext</span></span>
<span data-ttu-id="cc517-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="cc517-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="cc517-122">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="cc517-122">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="cc517-123">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="cc517-123">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="cc517-124">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="cc517-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="cc517-125">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="cc517-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="cc517-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="cc517-126">-ComputeNode</span></span>
<span data-ttu-id="cc517-127">Указывает вычислительный узел, как объект **PSComputeNode** , для которого этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc517-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="cc517-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="cc517-128">-ComputeNodeId</span></span>
<span data-ttu-id="cc517-129">Указывает идентификатор вычислительного узла, на котором этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc517-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="cc517-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc517-130">-DefaultProfile</span></span>
<span data-ttu-id="cc517-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc517-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc517-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cc517-132">-ExpiryTime</span></span>
<span data-ttu-id="cc517-133">Указывает время окончания срока действия новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc517-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="cc517-134">-Admin</span><span class="sxs-lookup"><span data-stu-id="cc517-134">-IsAdmin</span></span>
<span data-ttu-id="cc517-135">Указывает на то, что командлет создает учетную запись пользователя с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="cc517-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="cc517-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc517-136">-Name</span></span>
<span data-ttu-id="cc517-137">Указывает имя новой локальной учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="cc517-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="cc517-138">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="cc517-138">-Password</span></span>
<span data-ttu-id="cc517-139">Указывает пароль учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc517-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="cc517-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="cc517-140">-PoolId</span></span>
<span data-ttu-id="cc517-141">Указывает идентификатор пула, содержащего вычислительный узел, для которого нужно создать учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc517-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="cc517-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc517-142">CommonParameters</span></span>
<span data-ttu-id="cc517-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc517-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc517-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc517-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc517-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc517-145">INPUTS</span></span>

### <span data-ttu-id="cc517-146">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="cc517-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="cc517-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="cc517-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="cc517-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc517-148">OUTPUTS</span></span>

### <span data-ttu-id="cc517-149">System. void</span><span class="sxs-lookup"><span data-stu-id="cc517-149">System.Void</span></span>

## <span data-ttu-id="cc517-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc517-150">NOTES</span></span>

## <span data-ttu-id="cc517-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc517-151">RELATED LINKS</span></span>

[<span data-ttu-id="cc517-152">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="cc517-152">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="cc517-153">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="cc517-153">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="cc517-154">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="cc517-154">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="cc517-155">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="cc517-155">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


