---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245804"
---
# <span data-ttu-id="131a4-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="131a4-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="131a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="131a4-102">SYNOPSIS</span></span>
<span data-ttu-id="131a4-103">Удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="131a4-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="131a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="131a4-104">SYNTAX</span></span>

### <span data-ttu-id="131a4-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="131a4-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="131a4-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="131a4-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="131a4-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="131a4-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="131a4-108">DESCRIPTION</span></span>
<span data-ttu-id="131a4-109">Командлет **Remove-AzStorageObjectReplicationPolicy** удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="131a4-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="131a4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="131a4-110">EXAMPLES</span></span>

### <span data-ttu-id="131a4-111">Пример 1: Удаление политики репликации объектов с определенными policyId из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="131a4-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="131a4-112">Эта команда удаляет политику репликации объектов с определенными policyId из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="131a4-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="131a4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="131a4-113">PARAMETERS</span></span>

### <span data-ttu-id="131a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131a4-114">-DefaultProfile</span></span>
<span data-ttu-id="131a4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="131a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131a4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="131a4-116">-InputObject</span></span>
<span data-ttu-id="131a4-117">Объект политики репликации объектов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="131a4-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="131a4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="131a4-118">-PassThru</span></span>
<span data-ttu-id="131a4-119">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="131a4-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="131a4-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="131a4-120">-PolicyId</span></span>
<span data-ttu-id="131a4-121">Идентификатор политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="131a4-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="131a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="131a4-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="131a4-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131a4-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="131a4-124">-StorageAccount</span></span>
<span data-ttu-id="131a4-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="131a4-125">Storage account object</span></span>

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

### <span data-ttu-id="131a4-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="131a4-126">-StorageAccountName</span></span>
<span data-ttu-id="131a4-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="131a4-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131a4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="131a4-128">-Confirm</span></span>
<span data-ttu-id="131a4-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="131a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131a4-130">-WhatIf</span></span>
<span data-ttu-id="131a4-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="131a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131a4-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="131a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131a4-133">CommonParameters</span></span>
<span data-ttu-id="131a4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="131a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131a4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="131a4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131a4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="131a4-136">INPUTS</span></span>

### <span data-ttu-id="131a4-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="131a4-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="131a4-138">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="131a4-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="131a4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="131a4-139">OUTPUTS</span></span>

### <span data-ttu-id="131a4-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="131a4-140">System.Boolean</span></span>

## <span data-ttu-id="131a4-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="131a4-141">NOTES</span></span>

## <span data-ttu-id="131a4-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="131a4-142">RELATED LINKS</span></span>
