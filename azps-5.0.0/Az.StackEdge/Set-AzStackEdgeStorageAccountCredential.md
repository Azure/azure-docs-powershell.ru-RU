---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247198"
---
# <span data-ttu-id="bb81b-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bb81b-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bb81b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb81b-102">SYNOPSIS</span></span>
<span data-ttu-id="bb81b-103">Задает учетные данные учетной записи хранения для устройства.</span><span class="sxs-lookup"><span data-stu-id="bb81b-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="bb81b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb81b-104">SYNTAX</span></span>

### <span data-ttu-id="bb81b-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb81b-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb81b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb81b-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bb81b-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb81b-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb81b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb81b-108">DESCRIPTION</span></span>
<span data-ttu-id="bb81b-109">Командлет **Set-AzStackEdgeStorageAccountCredential** обновляет данные учетной записи хранения, соответствующие учетной записи хранения на пограничном устройстве стека.</span><span class="sxs-lookup"><span data-stu-id="bb81b-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="bb81b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb81b-110">EXAMPLES</span></span>

### <span data-ttu-id="bb81b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb81b-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="bb81b-112">Помогает при вращении клавиш доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bb81b-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="bb81b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb81b-113">PARAMETERS</span></span>

### <span data-ttu-id="bb81b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb81b-114">-AsJob</span></span>
<span data-ttu-id="bb81b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bb81b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb81b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb81b-116">-DefaultProfile</span></span>
<span data-ttu-id="bb81b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb81b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb81b-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="bb81b-118">-DeviceName</span></span>
<span data-ttu-id="bb81b-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="bb81b-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb81b-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="bb81b-120">-EncryptionKey</span></span>
<span data-ttu-id="bb81b-121">Ключ шифрования на пограничном устройстве</span><span class="sxs-lookup"><span data-stu-id="bb81b-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="bb81b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb81b-122">-InputObject</span></span>
<span data-ttu-id="bb81b-123">Объект input</span><span class="sxs-lookup"><span data-stu-id="bb81b-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb81b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb81b-124">-Name</span></span>
<span data-ttu-id="bb81b-125">Имя учетной записи хранения, которую нужно использовать</span><span class="sxs-lookup"><span data-stu-id="bb81b-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb81b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb81b-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb81b-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bb81b-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb81b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb81b-128">-ResourceId</span></span>
<span data-ttu-id="bb81b-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb81b-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb81b-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="bb81b-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="bb81b-131">предоставление ключа доступа учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="bb81b-131">provide storage account access key</span></span>

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

### <span data-ttu-id="bb81b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb81b-132">-Confirm</span></span>
<span data-ttu-id="bb81b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb81b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb81b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb81b-134">-WhatIf</span></span>
<span data-ttu-id="bb81b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb81b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb81b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb81b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb81b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb81b-137">CommonParameters</span></span>
<span data-ttu-id="bb81b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb81b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb81b-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb81b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb81b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb81b-140">INPUTS</span></span>

### <span data-ttu-id="bb81b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bb81b-141">System.String</span></span>

### <span data-ttu-id="bb81b-142">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bb81b-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bb81b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb81b-143">OUTPUTS</span></span>

### <span data-ttu-id="bb81b-144">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="bb81b-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="bb81b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb81b-145">NOTES</span></span>

## <span data-ttu-id="bb81b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb81b-146">RELATED LINKS</span></span>
