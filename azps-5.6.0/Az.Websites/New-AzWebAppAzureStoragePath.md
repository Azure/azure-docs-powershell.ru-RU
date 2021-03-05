---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: b30a7736c1d3971bcdd4d7b3b776b0c439e9395b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972355"
---
# <span data-ttu-id="f1fd9-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f1fd9-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="f1fd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1fd9-103">Создает объект, который представляет собой путь хранилища Azure, который будет установлен в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="f1fd9-104">Он предназначен для использования в качестве параметра (AzureStoragePath) для Set-AzWebApp и Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f1fd9-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="f1fd9-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f1fd9-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1fd9-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1fd9-106">DESCRIPTION</span></span>
<span data-ttu-id="f1fd9-107">Создание объекта, представляюного путь хранилища Azure, который должен быть установлен в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="f1fd9-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f1fd9-108">EXAMPLES</span></span>

### <span data-ttu-id="f1fd9-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f1fd9-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="f1fd9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="f1fd9-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="f1fd9-111">-AccessKey</span></span>
<span data-ttu-id="f1fd9-112">Ключ доступа к учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="f1fd9-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="f1fd9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1fd9-113">-AccountName</span></span>
<span data-ttu-id="f1fd9-114">Имя учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-114">Azure Storage account name.</span></span>
<span data-ttu-id="f1fd9-115">Например: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="f1fd9-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="f1fd9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1fd9-116">-DefaultProfile</span></span>
<span data-ttu-id="f1fd9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1fd9-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="f1fd9-118">-MountPath</span></span>
<span data-ttu-id="f1fd9-119">Путь в контейнере, где будет обначена указанная shareName</span><span class="sxs-lookup"><span data-stu-id="f1fd9-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="f1fd9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f1fd9-120">-Name</span></span>
<span data-ttu-id="f1fd9-121">Идентификатор свойства "Хранилище Azure".</span><span class="sxs-lookup"><span data-stu-id="f1fd9-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="f1fd9-122">Должен быть уникальным в пределах веб-приложения или слота</span><span class="sxs-lookup"><span data-stu-id="f1fd9-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="f1fd9-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f1fd9-123">-ShareName</span></span>
<span data-ttu-id="f1fd9-124">Имя области для крепления к контейнеру</span><span class="sxs-lookup"><span data-stu-id="f1fd9-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="f1fd9-125">-Type</span><span class="sxs-lookup"><span data-stu-id="f1fd9-125">-Type</span></span>
<span data-ttu-id="f1fd9-126">Тип учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="f1fd9-127">Контейнеры Windows поддерживают только файлы Azure</span><span class="sxs-lookup"><span data-stu-id="f1fd9-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="f1fd9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1fd9-128">-Confirm</span></span>
<span data-ttu-id="f1fd9-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1fd9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1fd9-130">-WhatIf</span></span>
<span data-ttu-id="f1fd9-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1fd9-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1fd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1fd9-133">CommonParameters</span></span>
<span data-ttu-id="f1fd9-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1fd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1fd9-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1fd9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1fd9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1fd9-136">INPUTS</span></span>

### <span data-ttu-id="f1fd9-137">Нет</span><span class="sxs-lookup"><span data-stu-id="f1fd9-137">None</span></span>

## <span data-ttu-id="f1fd9-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f1fd9-138">OUTPUTS</span></span>

### <span data-ttu-id="f1fd9-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="f1fd9-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="f1fd9-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f1fd9-140">NOTES</span></span>

## <span data-ttu-id="f1fd9-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1fd9-141">RELATED LINKS</span></span>
