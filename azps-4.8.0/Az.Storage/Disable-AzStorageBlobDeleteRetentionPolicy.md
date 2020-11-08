---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080214"
---
# <span data-ttu-id="75a16-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a16-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="75a16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75a16-102">SYNOPSIS</span></span>
<span data-ttu-id="75a16-103">Отключите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75a16-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="75a16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75a16-104">SYNTAX</span></span>

### <span data-ttu-id="75a16-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75a16-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a16-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="75a16-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75a16-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="75a16-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75a16-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a16-108">DESCRIPTION</span></span>
<span data-ttu-id="75a16-109">Командлет **Disable-AzStorageBlobDeleteRetentionPolicy** отключает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="75a16-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="75a16-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75a16-110">EXAMPLES</span></span>

### <span data-ttu-id="75a16-111">Пример 1: Отключение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="75a16-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="75a16-112">Эта команда отключает удаление политики хранения для службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="75a16-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="75a16-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75a16-113">PARAMETERS</span></span>

### <span data-ttu-id="75a16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a16-114">-DefaultProfile</span></span>
<span data-ttu-id="75a16-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75a16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a16-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="75a16-116">-PassThru</span></span>
<span data-ttu-id="75a16-117">Показать ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="75a16-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="75a16-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a16-118">-ResourceGroupName</span></span>
<span data-ttu-id="75a16-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="75a16-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="75a16-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75a16-120">-ResourceId</span></span>
<span data-ttu-id="75a16-121">Введите идентификатор ресурса учетной записи хранения или идентификатор ресурса свойств службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="75a16-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="75a16-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="75a16-122">-StorageAccount</span></span>
<span data-ttu-id="75a16-123">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="75a16-123">Storage account object</span></span>

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

### <span data-ttu-id="75a16-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="75a16-124">-StorageAccountName</span></span>
<span data-ttu-id="75a16-125">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="75a16-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="75a16-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75a16-126">-Confirm</span></span>
<span data-ttu-id="75a16-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75a16-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75a16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75a16-128">-WhatIf</span></span>
<span data-ttu-id="75a16-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75a16-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75a16-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75a16-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75a16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a16-131">CommonParameters</span></span>
<span data-ttu-id="75a16-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75a16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a16-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a16-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a16-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75a16-134">INPUTS</span></span>

### <span data-ttu-id="75a16-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="75a16-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="75a16-136">System. String</span><span class="sxs-lookup"><span data-stu-id="75a16-136">System.String</span></span>

## <span data-ttu-id="75a16-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a16-137">OUTPUTS</span></span>

### <span data-ttu-id="75a16-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75a16-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="75a16-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="75a16-139">NOTES</span></span>

## <span data-ttu-id="75a16-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75a16-140">RELATED LINKS</span></span>