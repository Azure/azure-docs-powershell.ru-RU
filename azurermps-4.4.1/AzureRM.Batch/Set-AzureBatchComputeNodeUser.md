---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565640"
---
# <span data-ttu-id="dca47-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dca47-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="dca47-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dca47-102">SYNOPSIS</span></span>
<span data-ttu-id="dca47-103">Изменяет свойства учетной записи на пакетно-вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="dca47-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca47-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dca47-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca47-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dca47-105">DESCRIPTION</span></span>
<span data-ttu-id="dca47-106">Командлет **Set-AzureBatchComputeNodeUser** изменяет свойства учетной записи пользователя на Пакетный вычислительный узел Azure.</span><span class="sxs-lookup"><span data-stu-id="dca47-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="dca47-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dca47-107">EXAMPLES</span></span>

### <span data-ttu-id="dca47-108">Пример 1: обновление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="dca47-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="dca47-109">Эта команда изменяет учетную запись пользователя с именем PFuller на узле COMPUTE node с указанным ИДЕНТИФИКАТОРом в пуле с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="dca47-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="dca47-110">Эта команда изменяет пароль учетной записи и время окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="dca47-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="dca47-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dca47-111">PARAMETERS</span></span>

### <span data-ttu-id="dca47-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="dca47-112">-BatchContext</span></span>
<span data-ttu-id="dca47-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="dca47-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="dca47-114">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="dca47-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="dca47-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="dca47-115">-ComputeNodeId</span></span>
<span data-ttu-id="dca47-116">Указывает идентификатор вычислительного узла, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dca47-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca47-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="dca47-117">-ExpiryTime</span></span>
<span data-ttu-id="dca47-118">Указывает время окончания срока действия учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="dca47-118">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="dca47-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dca47-119">-Name</span></span>
<span data-ttu-id="dca47-120">Указывает имя учетной записи пользователя, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dca47-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca47-121">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="dca47-121">-Password</span></span>
<span data-ttu-id="dca47-122">Указывает пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="dca47-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca47-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="dca47-123">-PoolId</span></span>
<span data-ttu-id="dca47-124">Указывает идентификатор пула, который содержит вычислительный узел, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="dca47-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dca47-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca47-125">-DefaultProfile</span></span>
<span data-ttu-id="dca47-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dca47-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca47-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca47-127">CommonParameters</span></span>
<span data-ttu-id="dca47-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dca47-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca47-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca47-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca47-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dca47-130">INPUTS</span></span>

### <span data-ttu-id="dca47-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="dca47-131">BatchAccountContext</span></span>
<span data-ttu-id="dca47-132">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="dca47-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="dca47-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dca47-133">OUTPUTS</span></span>

## <span data-ttu-id="dca47-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="dca47-134">NOTES</span></span>

## <span data-ttu-id="dca47-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dca47-135">RELATED LINKS</span></span>

[<span data-ttu-id="dca47-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="dca47-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="dca47-137">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dca47-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="dca47-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="dca47-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="dca47-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="dca47-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


