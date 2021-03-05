---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: c76c10d282d7a2b50cf0b35793cdda080d944740
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004627"
---
# <span data-ttu-id="88a3f-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88a3f-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="88a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="88a3f-103">Изменяет свойства учетной записи на узле пакетных вычислений.</span><span class="sxs-lookup"><span data-stu-id="88a3f-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="88a3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88a3f-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88a3f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="88a3f-106">**Cmdlet Set-AzBatchComputeNodeUser** изменяет свойства учетной записи пользователя в узле пакетных вычислений Azure.</span><span class="sxs-lookup"><span data-stu-id="88a3f-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="88a3f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="88a3f-108">Пример 1. Обновление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="88a3f-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="88a3f-109">Эта команда изменяет учетную запись пользователя с именем PFuller на узле вычислений с указанным ИД в пуле с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="88a3f-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="88a3f-110">Команда изменяет пароль учетной записи и срок ее действия.</span><span class="sxs-lookup"><span data-stu-id="88a3f-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="88a3f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88a3f-111">PARAMETERS</span></span>

### <span data-ttu-id="88a3f-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88a3f-112">-BatchContext</span></span>
<span data-ttu-id="88a3f-113">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="88a3f-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88a3f-114">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="88a3f-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88a3f-115">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="88a3f-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88a3f-116">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="88a3f-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88a3f-117">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88a3f-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88a3f-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="88a3f-118">-ComputeNodeId</span></span>
<span data-ttu-id="88a3f-119">Определяет код узла вычислений, на котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a3f-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88a3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88a3f-120">-DefaultProfile</span></span>
<span data-ttu-id="88a3f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88a3f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88a3f-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88a3f-122">-ExpiryTime</span></span>
<span data-ttu-id="88a3f-123">Указывает срок действия для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="88a3f-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="88a3f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="88a3f-124">-Name</span></span>
<span data-ttu-id="88a3f-125">Указывает имя учетной записи пользователя, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a3f-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="88a3f-126">-Password</span><span class="sxs-lookup"><span data-stu-id="88a3f-126">-Password</span></span>
<span data-ttu-id="88a3f-127">Пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="88a3f-127">Specifies the password for the user account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88a3f-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88a3f-128">-PoolId</span></span>
<span data-ttu-id="88a3f-129">Определяет код пула, который содержит узел вычислений, на котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88a3f-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88a3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88a3f-130">CommonParameters</span></span>
<span data-ttu-id="88a3f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88a3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88a3f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88a3f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88a3f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88a3f-133">INPUTS</span></span>

### <span data-ttu-id="88a3f-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88a3f-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88a3f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88a3f-135">OUTPUTS</span></span>

### <span data-ttu-id="88a3f-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="88a3f-136">System.Void</span></span>

## <span data-ttu-id="88a3f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88a3f-137">NOTES</span></span>

## <span data-ttu-id="88a3f-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88a3f-138">RELATED LINKS</span></span>

[<span data-ttu-id="88a3f-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88a3f-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88a3f-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88a3f-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88a3f-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88a3f-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88a3f-142">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="88a3f-142">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
