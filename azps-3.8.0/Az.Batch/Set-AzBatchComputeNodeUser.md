---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchComputeNodeUser.md
ms.openlocfilehash: ddf0632be8ea7749b733d21beecfdb539272d6c3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077249"
---
# <span data-ttu-id="88c15-101">Set-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88c15-101">Set-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="88c15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88c15-102">SYNOPSIS</span></span>
<span data-ttu-id="88c15-103">Изменяет свойства учетной записи на пакетно-вычислительном узле.</span><span class="sxs-lookup"><span data-stu-id="88c15-103">Modifies properties of an account on a Batch compute node.</span></span>

## <span data-ttu-id="88c15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88c15-104">SYNTAX</span></span>

```
Set-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <SecureString> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88c15-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c15-105">DESCRIPTION</span></span>
<span data-ttu-id="88c15-106">Командлет **Set-AzBatchComputeNodeUser** изменяет свойства учетной записи пользователя на Пакетный вычислительный узел Azure.</span><span class="sxs-lookup"><span data-stu-id="88c15-106">The **Set-AzBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="88c15-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88c15-107">EXAMPLES</span></span>

### <span data-ttu-id="88c15-108">Пример 1: обновление учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="88c15-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="88c15-109">Эта команда изменяет учетную запись пользователя с именем PFuller на узле COMPUTE node с указанным ИДЕНТИФИКАТОРом в пуле с именем ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="88c15-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="88c15-110">Эта команда изменяет пароль учетной записи и время окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="88c15-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="88c15-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88c15-111">PARAMETERS</span></span>

### <span data-ttu-id="88c15-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="88c15-112">-BatchContext</span></span>
<span data-ttu-id="88c15-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="88c15-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="88c15-114">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="88c15-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="88c15-115">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="88c15-115">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="88c15-116">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="88c15-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="88c15-117">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="88c15-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="88c15-118">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="88c15-118">-ComputeNodeId</span></span>
<span data-ttu-id="88c15-119">Указывает идентификатор вычислительного узла, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88c15-119">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88c15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c15-120">-DefaultProfile</span></span>
<span data-ttu-id="88c15-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88c15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88c15-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="88c15-122">-ExpiryTime</span></span>
<span data-ttu-id="88c15-123">Указывает время окончания срока действия учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="88c15-123">Specifies the expiry time for the user account.</span></span>

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

### <span data-ttu-id="88c15-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88c15-124">-Name</span></span>
<span data-ttu-id="88c15-125">Указывает имя учетной записи пользователя, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88c15-125">Specifies the name of the user account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="88c15-126">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="88c15-126">-Password</span></span>
<span data-ttu-id="88c15-127">Указывает пароль для учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="88c15-127">Specifies the password for the user account.</span></span>

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

### <span data-ttu-id="88c15-128">-PoolId</span><span class="sxs-lookup"><span data-stu-id="88c15-128">-PoolId</span></span>
<span data-ttu-id="88c15-129">Указывает идентификатор пула, который содержит вычислительный узел, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="88c15-129">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="88c15-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c15-130">CommonParameters</span></span>
<span data-ttu-id="88c15-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88c15-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c15-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88c15-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c15-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88c15-133">INPUTS</span></span>

### <span data-ttu-id="88c15-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="88c15-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="88c15-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88c15-135">OUTPUTS</span></span>

### <span data-ttu-id="88c15-136">System. void</span><span class="sxs-lookup"><span data-stu-id="88c15-136">System.Void</span></span>

## <span data-ttu-id="88c15-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="88c15-137">NOTES</span></span>

## <span data-ttu-id="88c15-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88c15-138">RELATED LINKS</span></span>

[<span data-ttu-id="88c15-139">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="88c15-139">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="88c15-140">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88c15-140">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88c15-141">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="88c15-141">Remove-AzBatchComputeNodeUser</span></span>](./Remove-AzBatchComputeNodeUser.md)

[<span data-ttu-id="88c15-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="88c15-142">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

