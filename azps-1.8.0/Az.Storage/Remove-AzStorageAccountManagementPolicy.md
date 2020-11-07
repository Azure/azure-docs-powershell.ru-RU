---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: d7290d44a1e6a08b79ccb5a0b5ff88ec482b4875
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728583"
---
# <span data-ttu-id="52af1-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="52af1-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="52af1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52af1-102">SYNOPSIS</span></span>
<span data-ttu-id="52af1-103">Удаление политики управления для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="52af1-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="52af1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52af1-104">SYNTAX</span></span>

### <span data-ttu-id="52af1-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52af1-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52af1-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="52af1-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52af1-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="52af1-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52af1-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="52af1-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52af1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52af1-109">DESCRIPTION</span></span>
<span data-ttu-id="52af1-110">Командлет **Remove-AzStorageAccountManagementPolicy** удаляет политику управления для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="52af1-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="52af1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52af1-111">EXAMPLES</span></span>

### <span data-ttu-id="52af1-112">Пример 1: Удаление политики управления для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52af1-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="52af1-113">Эта команда удаляет политику управления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52af1-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="52af1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52af1-114">PARAMETERS</span></span>

### <span data-ttu-id="52af1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52af1-115">-DefaultProfile</span></span>
<span data-ttu-id="52af1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52af1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52af1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52af1-117">-InputObject</span></span>
<span data-ttu-id="52af1-118">Объект управления для удаления</span><span class="sxs-lookup"><span data-stu-id="52af1-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52af1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52af1-119">-PassThru</span></span>
<span data-ttu-id="52af1-120">Указывает на то, что этот командлет возвращает **логическое значение** , отражающее успешное выполнение операции.</span><span class="sxs-lookup"><span data-stu-id="52af1-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="52af1-121">По умолчанию этот командлет не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="52af1-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="52af1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52af1-122">-ResourceGroupName</span></span>
<span data-ttu-id="52af1-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="52af1-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="52af1-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="52af1-124">-StorageAccount</span></span>
<span data-ttu-id="52af1-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="52af1-125">Storage account object</span></span>

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

### <span data-ttu-id="52af1-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52af1-126">-StorageAccountName</span></span>
<span data-ttu-id="52af1-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="52af1-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="52af1-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="52af1-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="52af1-129">Идентификатор ресурса учетной записи хранилища.</span><span class="sxs-lookup"><span data-stu-id="52af1-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52af1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52af1-130">-Confirm</span></span>
<span data-ttu-id="52af1-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52af1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52af1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52af1-132">-WhatIf</span></span>
<span data-ttu-id="52af1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52af1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52af1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52af1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52af1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52af1-135">CommonParameters</span></span>
<span data-ttu-id="52af1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52af1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52af1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52af1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52af1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52af1-138">INPUTS</span></span>

### <span data-ttu-id="52af1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="52af1-139">System.String</span></span>

## <span data-ttu-id="52af1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52af1-140">OUTPUTS</span></span>

### <span data-ttu-id="52af1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52af1-141">System.Boolean</span></span>

## <span data-ttu-id="52af1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="52af1-142">NOTES</span></span>

## <span data-ttu-id="52af1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52af1-143">RELATED LINKS</span></span>
