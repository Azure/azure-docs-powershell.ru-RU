---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 1e95eff4e93b1b7d55a099ad188fc196025cd06f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558544"
---
# <span data-ttu-id="bf493-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="bf493-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="bf493-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf493-102">SYNOPSIS</span></span>
<span data-ttu-id="bf493-103">Создание учетной записи пользователя на пакетном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="bf493-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf493-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf493-104">SYNTAX</span></span>

### <span data-ttu-id="bf493-105">Номер</span><span class="sxs-lookup"><span data-stu-id="bf493-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String>
 -Password <SecureString> [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf493-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="bf493-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <SecureString>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf493-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf493-107">DESCRIPTION</span></span>
<span data-ttu-id="bf493-108">Командлет **New-AzureBatchComputeNodeUser** создает учетную запись пользователя на пакетном кластере Azure.</span><span class="sxs-lookup"><span data-stu-id="bf493-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="bf493-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf493-109">EXAMPLES</span></span>

### <span data-ttu-id="bf493-110">Пример 1: создание учетной записи пользователя с правами администратора</span><span class="sxs-lookup"><span data-stu-id="bf493-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="bf493-111">Эта команда создает учетную запись пользователя на узле COMPUTE node с ИД ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="bf493-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="bf493-112">Узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="bf493-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="bf493-113">Имя пользователя: TestUser, пароль — это пароль, срок действия учетной записи истекает через семь дней, а учетная запись имеет учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="bf493-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="bf493-114">Пример 2: создание учетной записи пользователя на вычислительном узле с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="bf493-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="bf493-115">Эта команда получает узел COMPUTE node с именем ComputeNode01 с помощью командлета **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="bf493-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="bf493-116">Этот узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="bf493-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="bf493-117">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="bf493-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="bf493-118">Команда создает учетную запись пользователя с именем пользователя, TestUserand пароль.</span><span class="sxs-lookup"><span data-stu-id="bf493-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="bf493-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf493-119">PARAMETERS</span></span>

### <span data-ttu-id="bf493-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf493-120">-BatchContext</span></span>
<span data-ttu-id="bf493-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bf493-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf493-122">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="bf493-122">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bf493-123">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bf493-123">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bf493-124">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="bf493-124">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bf493-125">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bf493-125">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="bf493-126">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="bf493-126">-ComputeNode</span></span>
<span data-ttu-id="bf493-127">Указывает вычислительный узел, как объект **PSComputeNode** , для которого этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf493-127">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="bf493-128">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="bf493-128">-ComputeNodeId</span></span>
<span data-ttu-id="bf493-129">Указывает идентификатор вычислительного узла, на котором этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf493-129">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="bf493-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf493-130">-DefaultProfile</span></span>
<span data-ttu-id="bf493-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf493-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf493-132">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bf493-132">-ExpiryTime</span></span>
<span data-ttu-id="bf493-133">Указывает время окончания срока действия новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf493-133">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="bf493-134">-Admin</span><span class="sxs-lookup"><span data-stu-id="bf493-134">-IsAdmin</span></span>
<span data-ttu-id="bf493-135">Указывает на то, что командлет создает учетную запись пользователя с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="bf493-135">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="bf493-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf493-136">-Name</span></span>
<span data-ttu-id="bf493-137">Указывает имя новой локальной учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="bf493-137">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="bf493-138">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="bf493-138">-Password</span></span>
<span data-ttu-id="bf493-139">Указывает пароль учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf493-139">Specifies the user account password.</span></span>

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

### <span data-ttu-id="bf493-140">-PoolId</span><span class="sxs-lookup"><span data-stu-id="bf493-140">-PoolId</span></span>
<span data-ttu-id="bf493-141">Указывает идентификатор пула, содержащего вычислительный узел, для которого нужно создать учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf493-141">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="bf493-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf493-142">CommonParameters</span></span>
<span data-ttu-id="bf493-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf493-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf493-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf493-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf493-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf493-145">INPUTS</span></span>

### <span data-ttu-id="bf493-146">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="bf493-146">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="bf493-147">Параметры: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf493-147">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="bf493-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf493-148">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="bf493-149">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bf493-149">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="bf493-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf493-150">OUTPUTS</span></span>

### <span data-ttu-id="bf493-151">System. void</span><span class="sxs-lookup"><span data-stu-id="bf493-151">System.Void</span></span>

## <span data-ttu-id="bf493-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf493-152">NOTES</span></span>

## <span data-ttu-id="bf493-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf493-153">RELATED LINKS</span></span>

[<span data-ttu-id="bf493-154">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bf493-154">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bf493-155">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="bf493-155">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="bf493-156">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="bf493-156">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="bf493-157">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="bf493-157">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


