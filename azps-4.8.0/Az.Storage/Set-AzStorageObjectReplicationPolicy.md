---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236524"
---
# <span data-ttu-id="3c7f3-101">Set-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3c7f3-101">Set-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="3c7f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c7f3-103">Создает или обновляет указанную политику репликации объектов в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-103">Creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="3c7f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c7f3-104">SYNTAX</span></span>

### <span data-ttu-id="3c7f3-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c7f3-105">AccountName (Default)</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c7f3-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="3c7f3-106">PolicyObject</span></span>
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c7f3-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3c7f3-107">AccountObject</span></span>
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c7f3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7f3-108">DESCRIPTION</span></span>
<span data-ttu-id="3c7f3-109">Командлет **Set-AzStorageObjectReplicationPolicy** создает или обновляет указанную политику репликации объектов в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-109">The **Set-AzStorageObjectReplicationPolicy** cmdlet creates or updates the specified object replication policy in a Storage account.</span></span>

## <span data-ttu-id="3c7f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c7f3-110">EXAMPLES</span></span>

### <span data-ttu-id="3c7f3-111">Пример 1: Настройка политики репликации объектов для конечной и исходной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-111">Example 1: Set object replication policy to both destination and source account.</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

<span data-ttu-id="3c7f3-112">Эта команда задает для политики репликации объектов конечную и исходную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-112">This command sets object replication policy to both destination and source account.</span></span>
<span data-ttu-id="3c7f3-113">Сначала создайте правила политики репликации объектов 2 и настройте политику, указав 2 правила для конечной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-113">First create 2 object replication policy rules, and set policy with the 2 rules to destination account.</span></span> <span data-ttu-id="3c7f3-114">Затем настройте политику репликации объектов от конечной учетной записи на исходную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-114">Then set the object replication policy from destination account to source account.</span></span>

## <span data-ttu-id="3c7f3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c7f3-115">PARAMETERS</span></span>

### <span data-ttu-id="3c7f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c7f3-116">-DefaultProfile</span></span>
<span data-ttu-id="3c7f3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c7f3-118">-DestinationAccount</span><span class="sxs-lookup"><span data-stu-id="3c7f3-118">-DestinationAccount</span></span>
<span data-ttu-id="3c7f3-119">DestinationAccount политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-119">Object Replication Policy DestinationAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c7f3-120">-InputObject</span></span>
<span data-ttu-id="3c7f3-121">Объект политики репликации объектов для задания указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-121">Object Replication Policy Object to Set to the specified Account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-122">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="3c7f3-122">-PolicyId</span></span>
<span data-ttu-id="3c7f3-123">Идентификатор политики репликации объектов. Это должен быть GUID или "default".</span><span class="sxs-lookup"><span data-stu-id="3c7f3-123">Object Replication Policy Id. It should be a GUID or 'default'.</span></span>
<span data-ttu-id="3c7f3-124">Если PolicyId не введено, будет использоваться значение по умолчанию, которое означает, что вы можете создать новую политику, и идентификатор новой политики будет возвращен в созданной политике.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-124">If not input the PolicyId, will use 'default', which means to create a new policy and the Id of the new policy will be returned in the created policy.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c7f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c7f3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-127">-Правило</span><span class="sxs-lookup"><span data-stu-id="3c7f3-127">-Rule</span></span>
<span data-ttu-id="3c7f3-128">Правила политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-128">Object Replication Policy Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-129">-SourceAccount</span><span class="sxs-lookup"><span data-stu-id="3c7f3-129">-SourceAccount</span></span>
<span data-ttu-id="3c7f3-130">SourceAccount политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-130">Object Replication Policy SourceAccount.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c7f3-131">-StorageAccount</span></span>
<span data-ttu-id="3c7f3-132">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="3c7f3-132">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3c7f3-133">-StorageAccountName</span></span>
<span data-ttu-id="3c7f3-134">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-134">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c7f3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c7f3-135">-Confirm</span></span>
<span data-ttu-id="3c7f3-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c7f3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c7f3-137">-WhatIf</span></span>
<span data-ttu-id="3c7f3-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c7f3-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c7f3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c7f3-140">CommonParameters</span></span>
<span data-ttu-id="3c7f3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c7f3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c7f3-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c7f3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c7f3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c7f3-143">INPUTS</span></span>

### <span data-ttu-id="3c7f3-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c7f3-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3c7f3-145">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3c7f3-145">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="3c7f3-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c7f3-146">OUTPUTS</span></span>

### <span data-ttu-id="3c7f3-147">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="3c7f3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="3c7f3-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c7f3-148">NOTES</span></span>

## <span data-ttu-id="3c7f3-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c7f3-149">RELATED LINKS</span></span>
