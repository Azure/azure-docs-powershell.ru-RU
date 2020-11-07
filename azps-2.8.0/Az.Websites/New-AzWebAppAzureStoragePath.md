---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: f4ed396f1abbd8a123bb0e765e288c1ae55d25fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907550"
---
# <span data-ttu-id="36d72-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="36d72-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="36d72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36d72-102">SYNOPSIS</span></span>
<span data-ttu-id="36d72-103">Создает объект, представляющий путь к хранилищу Azure, который нужно подключить к веб-приложению.</span><span class="sxs-lookup"><span data-stu-id="36d72-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="36d72-104">Он предназначен для использования в качестве параметра (-AzureStoragePath) для Set-AzWebApp и Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="36d72-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="36d72-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36d72-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36d72-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d72-106">DESCRIPTION</span></span>
<span data-ttu-id="36d72-107">Создает объект, представляющий путь к хранилищу Azure, который нужно подключить в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="36d72-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="36d72-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36d72-108">EXAMPLES</span></span>

### <span data-ttu-id="36d72-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36d72-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="36d72-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36d72-110">PARAMETERS</span></span>

### <span data-ttu-id="36d72-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="36d72-111">-AccessKey</span></span>
<span data-ttu-id="36d72-112">Ключ доступа к учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="36d72-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="36d72-113">-AccountName</span></span>
<span data-ttu-id="36d72-114">Имя учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="36d72-114">Azure Storage account name.</span></span>
<span data-ttu-id="36d72-115">Например: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="36d72-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d72-116">-DefaultProfile</span></span>
<span data-ttu-id="36d72-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36d72-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36d72-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="36d72-118">-MountPath</span></span>
<span data-ttu-id="36d72-119">Путь в контейнере, в котором будет предоставлен общий доступ, указанный в ShareName</span><span class="sxs-lookup"><span data-stu-id="36d72-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36d72-120">-Name</span></span>
<span data-ttu-id="36d72-121">Идентификатор свойства хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="36d72-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="36d72-122">Должно быть уникальным в пределах веб-приложения или ячейки</span><span class="sxs-lookup"><span data-stu-id="36d72-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-123">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="36d72-123">-ShareName</span></span>
<span data-ttu-id="36d72-124">Имя общего доступа, которое нужно подключить к контейнеру</span><span class="sxs-lookup"><span data-stu-id="36d72-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="36d72-125">-Type</span></span>
<span data-ttu-id="36d72-126">Тип учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="36d72-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="36d72-127">Контейнеры Windows поддерживают только файлы Azure.</span><span class="sxs-lookup"><span data-stu-id="36d72-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d72-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36d72-128">-Confirm</span></span>
<span data-ttu-id="36d72-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36d72-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d72-130">-WhatIf</span></span>
<span data-ttu-id="36d72-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36d72-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36d72-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36d72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d72-133">CommonParameters</span></span>
<span data-ttu-id="36d72-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36d72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d72-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d72-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d72-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36d72-136">INPUTS</span></span>

### <span data-ttu-id="36d72-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="36d72-137">None</span></span>

## <span data-ttu-id="36d72-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d72-138">OUTPUTS</span></span>

### <span data-ttu-id="36d72-139">Microsoft. Azure. Commands. Apps. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="36d72-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="36d72-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="36d72-140">NOTES</span></span>

## <span data-ttu-id="36d72-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d72-141">RELATED LINKS</span></span>
