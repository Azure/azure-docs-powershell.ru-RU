---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246348"
---
# <span data-ttu-id="fa13e-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="fa13e-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="fa13e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fa13e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa13e-103">Получение свойств службы для файловых служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fa13e-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="fa13e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fa13e-104">SYNTAX</span></span>

### <span data-ttu-id="fa13e-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa13e-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa13e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fa13e-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa13e-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="fa13e-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa13e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa13e-108">DESCRIPTION</span></span>
<span data-ttu-id="fa13e-109">Командлет **Get-AzStorageFileServiceProperty** получает свойства службы для файловых служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="fa13e-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="fa13e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fa13e-110">EXAMPLES</span></span>

### <span data-ttu-id="fa13e-111">Пример 1: получение свойства файловых служб хранилища Azure для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fa13e-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="fa13e-112">Эта команда получает свойство файловых служб для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa13e-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="fa13e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fa13e-113">PARAMETERS</span></span>

### <span data-ttu-id="fa13e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa13e-114">-DefaultProfile</span></span>
<span data-ttu-id="fa13e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa13e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa13e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa13e-116">-ResourceGroupName</span></span>
<span data-ttu-id="fa13e-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa13e-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa13e-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa13e-118">-ResourceId</span></span>
<span data-ttu-id="fa13e-119">Введите идентификатор ресурса учетной записи хранилища или идентификатор ресурса свойств службы файлов.</span><span class="sxs-lookup"><span data-stu-id="fa13e-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa13e-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa13e-120">-StorageAccount</span></span>
<span data-ttu-id="fa13e-121">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="fa13e-121">Storage account object</span></span>

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

### <span data-ttu-id="fa13e-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fa13e-122">-StorageAccountName</span></span>
<span data-ttu-id="fa13e-123">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="fa13e-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="fa13e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa13e-124">CommonParameters</span></span>
<span data-ttu-id="fa13e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fa13e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa13e-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa13e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa13e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fa13e-127">INPUTS</span></span>

### <span data-ttu-id="fa13e-128">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa13e-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fa13e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fa13e-129">System.String</span></span>

## <span data-ttu-id="fa13e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa13e-130">OUTPUTS</span></span>

### <span data-ttu-id="fa13e-131">Microsoft. Azure. Commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="fa13e-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="fa13e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="fa13e-132">NOTES</span></span>

## <span data-ttu-id="fa13e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa13e-133">RELATED LINKS</span></span>
