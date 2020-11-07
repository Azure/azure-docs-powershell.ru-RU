---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 03e77346c14e095a11720b8cdaf930eaaa397f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728671"
---
# <span data-ttu-id="e192c-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="e192c-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="e192c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e192c-102">SYNOPSIS</span></span>
<span data-ttu-id="e192c-103">Получение свойств службы для служб больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e192c-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="e192c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e192c-104">SYNTAX</span></span>

### <span data-ttu-id="e192c-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e192c-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e192c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e192c-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e192c-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="e192c-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e192c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e192c-108">DESCRIPTION</span></span>
<span data-ttu-id="e192c-109">Командлет **Get-AzStorageBlobServiceProperty** получает свойства службы для служб BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="e192c-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="e192c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e192c-110">EXAMPLES</span></span>

### <span data-ttu-id="e192c-111">Пример 1: получение свойства служб BLOB хранилища Azure для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e192c-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="e192c-112">Эта команда возвращает свойство "службы BLOB" указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e192c-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="e192c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e192c-113">PARAMETERS</span></span>

### <span data-ttu-id="e192c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e192c-114">-DefaultProfile</span></span>
<span data-ttu-id="e192c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e192c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e192c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e192c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e192c-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e192c-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="e192c-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e192c-118">-ResourceId</span></span>
<span data-ttu-id="e192c-119">Идентификатор ресурса свойств службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="e192c-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="e192c-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e192c-120">-StorageAccount</span></span>
<span data-ttu-id="e192c-121">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e192c-121">Storage account object</span></span>

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

### <span data-ttu-id="e192c-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e192c-122">-StorageAccountName</span></span>
<span data-ttu-id="e192c-123">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e192c-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="e192c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e192c-124">CommonParameters</span></span>
<span data-ttu-id="e192c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e192c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e192c-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e192c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e192c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e192c-127">INPUTS</span></span>

### <span data-ttu-id="e192c-128">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e192c-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e192c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e192c-129">System.String</span></span>

## <span data-ttu-id="e192c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e192c-130">OUTPUTS</span></span>

### <span data-ttu-id="e192c-131">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="e192c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="e192c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e192c-132">NOTES</span></span>

## <span data-ttu-id="e192c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e192c-133">RELATED LINKS</span></span>
