---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565657"
---
# <span data-ttu-id="46e5e-101">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="46e5e-101">New-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="46e5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="46e5e-103">Создание учетной записи пользователя на пакетном вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="46e5e-103">Creates a user account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46e5e-104">SYNTAX</span></span>

### <span data-ttu-id="46e5e-105">Номер</span><span class="sxs-lookup"><span data-stu-id="46e5e-105">Id</span></span>
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e5e-106">ParentObject</span><span class="sxs-lookup"><span data-stu-id="46e5e-106">ParentObject</span></span>
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46e5e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e5e-107">DESCRIPTION</span></span>
<span data-ttu-id="46e5e-108">Командлет **New-AzureBatchComputeNodeUser** создает учетную запись пользователя на пакетном кластере Azure.</span><span class="sxs-lookup"><span data-stu-id="46e5e-108">The **New-AzureBatchComputeNodeUser** cmdlet creates a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="46e5e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46e5e-109">EXAMPLES</span></span>

### <span data-ttu-id="46e5e-110">Пример 1: создание учетной записи пользователя с правами администратора</span><span class="sxs-lookup"><span data-stu-id="46e5e-110">Example 1: Create a user account that has administrative credentials</span></span>
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

<span data-ttu-id="46e5e-111">Эта команда создает учетную запись пользователя на узле COMPUTE node с ИД ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="46e5e-111">This command creates a user account on the compute node that has the ID ComputeNode01.</span></span>
<span data-ttu-id="46e5e-112">Узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="46e5e-112">The node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="46e5e-113">Имя пользователя: TestUser, пароль — это пароль, срок действия учетной записи истекает через семь дней, а учетная запись имеет учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="46e5e-113">The user name is TestUser, the password is Password, the account expires in seven days, and the account is has administrative credentials.</span></span>

### <span data-ttu-id="46e5e-114">Пример 2: создание учетной записи пользователя на вычислительном узле с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="46e5e-114">Example 2: Create a user account on a compute node by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

<span data-ttu-id="46e5e-115">Эта команда получает узел COMPUTE node с именем ComputeNode01 с помощью командлета **Get-AzureBatchComputeNode** .</span><span class="sxs-lookup"><span data-stu-id="46e5e-115">This command gets the compute node named ComputeNode01 by using the **Get-AzureBatchComputeNode** cmdlet.</span></span>
<span data-ttu-id="46e5e-116">Этот узел находится в пуле с ИДЕНТИФИКАТОРом MyPool01.</span><span class="sxs-lookup"><span data-stu-id="46e5e-116">That node is in the pool that has the ID MyPool01.</span></span>
<span data-ttu-id="46e5e-117">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="46e5e-117">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="46e5e-118">Команда создает учетную запись пользователя с именем пользователя, TestUserand пароль.</span><span class="sxs-lookup"><span data-stu-id="46e5e-118">The command creates a user account that has the user name TestUserand the password Password.</span></span>

## <span data-ttu-id="46e5e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46e5e-119">PARAMETERS</span></span>

### <span data-ttu-id="46e5e-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="46e5e-120">-BatchContext</span></span>
<span data-ttu-id="46e5e-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="46e5e-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="46e5e-122">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="46e5e-122">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="46e5e-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="46e5e-123">-ComputeNode</span></span>
<span data-ttu-id="46e5e-124">Указывает вычислительный узел, как объект **PSComputeNode** , для которого этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e5e-124">Specifies the compute node, as a **PSComputeNode** object, on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="46e5e-125">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="46e5e-125">-ComputeNodeId</span></span>
<span data-ttu-id="46e5e-126">Указывает идентификатор вычислительного узла, на котором этот командлет создает учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e5e-126">Specifies the ID of the compute node on which this cmdlet creates a user account.</span></span>

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

### <span data-ttu-id="46e5e-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="46e5e-127">-ExpiryTime</span></span>
<span data-ttu-id="46e5e-128">Указывает время окончания срока действия новой учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e5e-128">Specifies the expiry time for the new user account.</span></span>

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

### <span data-ttu-id="46e5e-129">-Admin</span><span class="sxs-lookup"><span data-stu-id="46e5e-129">-IsAdmin</span></span>
<span data-ttu-id="46e5e-130">Указывает на то, что командлет создает учетную запись пользователя с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="46e5e-130">Indicates that the cmdlet creates a user account that has administrative credentials.</span></span>

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

### <span data-ttu-id="46e5e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46e5e-131">-Name</span></span>
<span data-ttu-id="46e5e-132">Указывает имя новой локальной учетной записи Windows.</span><span class="sxs-lookup"><span data-stu-id="46e5e-132">Specifies the name of the new local Windows account.</span></span>

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

### <span data-ttu-id="46e5e-133">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="46e5e-133">-Password</span></span>
<span data-ttu-id="46e5e-134">Указывает пароль учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e5e-134">Specifies the user account password.</span></span>

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

### <span data-ttu-id="46e5e-135">-PoolId</span><span class="sxs-lookup"><span data-stu-id="46e5e-135">-PoolId</span></span>
<span data-ttu-id="46e5e-136">Указывает идентификатор пула, содержащего вычислительный узел, для которого нужно создать учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="46e5e-136">Specifies the ID of the pool that contains the compute node on which to create the user account.</span></span>

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

### <span data-ttu-id="46e5e-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e5e-137">-DefaultProfile</span></span>
<span data-ttu-id="46e5e-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46e5e-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46e5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e5e-139">CommonParameters</span></span>
<span data-ttu-id="46e5e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46e5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e5e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e5e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e5e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46e5e-142">INPUTS</span></span>

### <span data-ttu-id="46e5e-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="46e5e-143">BatchAccountContext</span></span>
<span data-ttu-id="46e5e-144">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="46e5e-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="46e5e-145">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="46e5e-145">PSComputeNode</span></span>
<span data-ttu-id="46e5e-146">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="46e5e-146">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="46e5e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e5e-147">OUTPUTS</span></span>

## <span data-ttu-id="46e5e-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="46e5e-148">NOTES</span></span>

## <span data-ttu-id="46e5e-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46e5e-149">RELATED LINKS</span></span>

[<span data-ttu-id="46e5e-150">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="46e5e-150">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="46e5e-151">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="46e5e-151">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="46e5e-152">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="46e5e-152">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="46e5e-153">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="46e5e-153">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


