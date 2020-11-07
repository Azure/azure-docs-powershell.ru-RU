---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6fb398e44b2e6de8a0d00e9a8d737916fafa2472
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734721"
---
# <span data-ttu-id="b2623-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b2623-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="b2623-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2623-102">SYNOPSIS</span></span>
<span data-ttu-id="b2623-103">Изменяет свойства учетной записи на пакетно-вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="b2623-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2623-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2623-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2623-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2623-105">DESCRIPTION</span></span>
<span data-ttu-id="b2623-106">Командлет **Set-AzureBatchComputeNodeUser** изменяет свойства учетной записи пользователя на Пакетный вычислительный узел Azure.</span><span class="sxs-lookup"><span data-stu-id="b2623-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="b2623-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2623-107">EXAMPLES</span></span>

### <span data-ttu-id="b2623-108">Пример 1: обновление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="b2623-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="b2623-109">Эта команда изменяет учетную запись пользователя с именем PFuller на узле COMPUTE node с указанным ИДЕНТИФИКАТОРом в пуле с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="b2623-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="b2623-110">Эта команда изменяет пароль учетной записи и время окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="b2623-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="b2623-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2623-111">PARAMETERS</span></span>

### <span data-ttu-id="b2623-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b2623-112">-BatchContext</span></span>
<span data-ttu-id="b2623-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b2623-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b2623-114">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="b2623-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b2623-115">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="b2623-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b2623-116">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="b2623-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b2623-117">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b2623-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="b2623-118">-ComputeNodeId</span></span>
<span data-ttu-id="b2623-119">Указывает идентификатор вычислительного узла, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2623-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2623-120">-DefaultProfile</span></span>
<span data-ttu-id="b2623-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2623-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b2623-122">-ExpiryTime</span></span>
<span data-ttu-id="b2623-123">Указывает время окончания срока действия учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="b2623-123">Specifies the expiry time for the user account.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2623-124">-Name</span></span>
<span data-ttu-id="b2623-125">Указывает имя учетной записи пользователя, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2623-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="b2623-126">-Password</span></span>
<span data-ttu-id="b2623-127">Указывает пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="b2623-127">Specifies the password for the user account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="b2623-128">-PoolId</span></span>
<span data-ttu-id="b2623-129">Указывает идентификатор пула, который содержит вычислительный узел, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2623-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2623-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2623-130">CommonParameters</span></span>
<span data-ttu-id="b2623-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2623-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2623-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2623-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2623-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2623-133">INPUTS</span></span>

### <span data-ttu-id="b2623-134">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b2623-134">BatchAccountContext</span></span>
<span data-ttu-id="b2623-135">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2623-135">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b2623-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2623-136">OUTPUTS</span></span>

## <span data-ttu-id="b2623-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2623-137">NOTES</span></span>

## <span data-ttu-id="b2623-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2623-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2623-139">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b2623-139">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b2623-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b2623-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b2623-141">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="b2623-141">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="b2623-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b2623-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


