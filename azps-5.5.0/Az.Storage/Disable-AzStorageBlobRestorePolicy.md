---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222945"
---
# <span data-ttu-id="e8f2e-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e8f2e-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="e8f2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f2e-103">Отключение политики восстановления BLOB-то в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="e8f2e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8f2e-104">SYNTAX</span></span>

### <span data-ttu-id="e8f2e-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8f2e-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f2e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e8f2e-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f2e-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f2e-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f2e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f2e-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f2e-109">**Cmdlet Disable-AzStorageBlobRestorePolicy** отключает политику восстановления BLOB-приложений для службы BLOB-приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e8f2e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8f2e-110">EXAMPLES</span></span>

### <span data-ttu-id="e8f2e-111">Пример 1. Отключение политики восстановления BLOB-хранилищ Azure для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e8f2e-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="e8f2e-112">Эта команда отключает политику восстановления BLOB-хранилищ Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="e8f2e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8f2e-113">PARAMETERS</span></span>

### <span data-ttu-id="e8f2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f2e-114">-DefaultProfile</span></span>
<span data-ttu-id="e8f2e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f2e-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8f2e-116">-PassThru</span></span>
<span data-ttu-id="e8f2e-117">Отображение свойств службы</span><span class="sxs-lookup"><span data-stu-id="e8f2e-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="e8f2e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f2e-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8f2e-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8f2e-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f2e-120">-ResourceId</span></span>
<span data-ttu-id="e8f2e-121">Ввести ИД ресурса учетной записи хранения или свойства ресурса службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f2e-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8f2e-122">-StorageAccount</span></span>
<span data-ttu-id="e8f2e-123">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e8f2e-123">Storage account object</span></span>

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

### <span data-ttu-id="e8f2e-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8f2e-124">-StorageAccountName</span></span>
<span data-ttu-id="e8f2e-125">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-125">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f2e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8f2e-126">-Confirm</span></span>
<span data-ttu-id="e8f2e-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f2e-128">-WhatIf</span></span>
<span data-ttu-id="e8f2e-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f2e-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f2e-131">CommonParameters</span></span>
<span data-ttu-id="e8f2e-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f2e-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f2e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f2e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8f2e-134">INPUTS</span></span>

### <span data-ttu-id="e8f2e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e8f2e-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e8f2e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e8f2e-136">System.String</span></span>

## <span data-ttu-id="e8f2e-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8f2e-137">OUTPUTS</span></span>

### <span data-ttu-id="e8f2e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="e8f2e-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="e8f2e-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8f2e-139">NOTES</span></span>

## <span data-ttu-id="e8f2e-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8f2e-140">RELATED LINKS</span></span>
