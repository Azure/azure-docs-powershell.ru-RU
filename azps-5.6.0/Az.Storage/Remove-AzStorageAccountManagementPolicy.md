---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 671a83ee392f59dc27cff6cc34eeb7df054b3fbf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002291"
---
# <span data-ttu-id="c8326-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c8326-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="c8326-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8326-102">SYNOPSIS</span></span>
<span data-ttu-id="c8326-103">Удаляет политику управления учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="c8326-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="c8326-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8326-104">SYNTAX</span></span>

### <span data-ttu-id="c8326-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8326-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8326-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c8326-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8326-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c8326-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8326-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="c8326-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8326-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8326-109">DESCRIPTION</span></span>
<span data-ttu-id="c8326-110">Для удаления учетной записи хранилища Azure удаляется политика управления **Remove-AzStorageAccountManagementPolicy.**</span><span class="sxs-lookup"><span data-stu-id="c8326-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="c8326-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8326-111">EXAMPLES</span></span>

### <span data-ttu-id="c8326-112">Пример 1. Удаление политики управления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c8326-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="c8326-113">Эта команда удаляет политику управления учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c8326-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="c8326-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8326-114">PARAMETERS</span></span>

### <span data-ttu-id="c8326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8326-115">-DefaultProfile</span></span>
<span data-ttu-id="c8326-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8326-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8326-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8326-117">-InputObject</span></span>
<span data-ttu-id="c8326-118">Объект управления, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="c8326-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="c8326-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8326-119">-PassThru</span></span>
<span data-ttu-id="c8326-120">Указывает на то, что этот cmdlet возвращает **boolean,** который отражает успешность операции.</span><span class="sxs-lookup"><span data-stu-id="c8326-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c8326-121">По умолчанию этот cmdlet не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c8326-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c8326-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8326-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8326-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8326-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8326-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8326-124">-StorageAccount</span></span>
<span data-ttu-id="c8326-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c8326-125">Storage account object</span></span>

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

### <span data-ttu-id="c8326-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8326-126">-StorageAccountName</span></span>
<span data-ttu-id="c8326-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c8326-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="c8326-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c8326-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="c8326-129">ИД ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c8326-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="c8326-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8326-130">-Confirm</span></span>
<span data-ttu-id="c8326-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8326-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8326-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8326-132">-WhatIf</span></span>
<span data-ttu-id="c8326-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8326-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8326-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8326-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8326-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8326-135">CommonParameters</span></span>
<span data-ttu-id="c8326-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8326-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8326-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8326-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8326-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8326-138">INPUTS</span></span>

### <span data-ttu-id="c8326-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c8326-139">System.String</span></span>

## <span data-ttu-id="c8326-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8326-140">OUTPUTS</span></span>

### <span data-ttu-id="c8326-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8326-141">System.Boolean</span></span>

## <span data-ttu-id="c8326-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8326-142">NOTES</span></span>

## <span data-ttu-id="c8326-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8326-143">RELATED LINKS</span></span>
