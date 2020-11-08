---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: 4c42fe6e612f30ab622a0a04498e5474f27690e9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236531"
---
# <span data-ttu-id="87eaa-101">Remove-AzStorageObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="87eaa-101">Remove-AzStorageObjectReplicationPolicy</span></span>

## <span data-ttu-id="87eaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="87eaa-103">Удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87eaa-103">Removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="87eaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87eaa-104">SYNTAX</span></span>

### <span data-ttu-id="87eaa-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87eaa-105">AccountName (Default)</span></span>
```
Remove-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -PolicyId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="87eaa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="87eaa-106">AccountObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> -PolicyId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87eaa-107">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="87eaa-107">PolicyObject</span></span>
```
Remove-AzStorageObjectReplicationPolicy -InputObject <PSObjectReplicationPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87eaa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87eaa-108">DESCRIPTION</span></span>
<span data-ttu-id="87eaa-109">Командлет **Remove-AzStorageObjectReplicationPolicy** удаляет указанную политику репликации объектов из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87eaa-109">The **Remove-AzStorageObjectReplicationPolicy** cmdlet removes the specified object replication policy from a Storage account.</span></span>

## <span data-ttu-id="87eaa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87eaa-110">EXAMPLES</span></span>

### <span data-ttu-id="87eaa-111">Пример 1: Удаление политики репликации объектов с определенными policyId из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87eaa-111">Example 1: Remove an object replication policy with specific policyId from a storage account.</span></span>
```
Remove-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PolicyId $policyId
```

<span data-ttu-id="87eaa-112">Эта команда удаляет политику репликации объектов с определенными policyId из учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87eaa-112">This command removes an object replication policy with specific policyId from a storage account.</span></span>

## <span data-ttu-id="87eaa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87eaa-113">PARAMETERS</span></span>

### <span data-ttu-id="87eaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eaa-114">-DefaultProfile</span></span>
<span data-ttu-id="87eaa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87eaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87eaa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87eaa-116">-InputObject</span></span>
<span data-ttu-id="87eaa-117">Объект политики репликации объектов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="87eaa-117">Object Replication Policy object to Delete.</span></span>

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

### <span data-ttu-id="87eaa-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87eaa-118">-PassThru</span></span>
<span data-ttu-id="87eaa-119">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="87eaa-119">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="87eaa-120">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="87eaa-120">-PolicyId</span></span>
<span data-ttu-id="87eaa-121">Идентификатор политики репликации объектов.</span><span class="sxs-lookup"><span data-stu-id="87eaa-121">Object Replication Policy Id.</span></span>

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

### <span data-ttu-id="87eaa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87eaa-122">-ResourceGroupName</span></span>
<span data-ttu-id="87eaa-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87eaa-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="87eaa-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="87eaa-124">-StorageAccount</span></span>
<span data-ttu-id="87eaa-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="87eaa-125">Storage account object</span></span>

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

### <span data-ttu-id="87eaa-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87eaa-126">-StorageAccountName</span></span>
<span data-ttu-id="87eaa-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="87eaa-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="87eaa-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87eaa-128">-Confirm</span></span>
<span data-ttu-id="87eaa-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87eaa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87eaa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87eaa-130">-WhatIf</span></span>
<span data-ttu-id="87eaa-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87eaa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87eaa-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87eaa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87eaa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eaa-133">CommonParameters</span></span>
<span data-ttu-id="87eaa-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87eaa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eaa-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eaa-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eaa-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87eaa-136">INPUTS</span></span>

### <span data-ttu-id="87eaa-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="87eaa-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="87eaa-138">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="87eaa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy</span></span>

## <span data-ttu-id="87eaa-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87eaa-139">OUTPUTS</span></span>

### <span data-ttu-id="87eaa-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87eaa-140">System.Boolean</span></span>

## <span data-ttu-id="87eaa-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="87eaa-141">NOTES</span></span>

## <span data-ttu-id="87eaa-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87eaa-142">RELATED LINKS</span></span>
