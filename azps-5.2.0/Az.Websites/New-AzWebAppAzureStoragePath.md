---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392439"
---
# <span data-ttu-id="4119f-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="4119f-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="4119f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4119f-102">SYNOPSIS</span></span>
<span data-ttu-id="4119f-103">Создает объект, который представляет собой путь хранилища Azure, который будет установлен в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="4119f-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="4119f-104">Он предназначен для использования в качестве параметра (AzureStoragePath) для Set-AzWebApp и Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4119f-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="4119f-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4119f-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4119f-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4119f-106">DESCRIPTION</span></span>
<span data-ttu-id="4119f-107">Создание объекта, представляюного путь хранилища Azure, который должен быть установлен в веб-приложении.</span><span class="sxs-lookup"><span data-stu-id="4119f-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="4119f-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4119f-108">EXAMPLES</span></span>

### <span data-ttu-id="4119f-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4119f-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="4119f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4119f-110">PARAMETERS</span></span>

### <span data-ttu-id="4119f-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="4119f-111">-AccessKey</span></span>
<span data-ttu-id="4119f-112">Ключ доступа к учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="4119f-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="4119f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4119f-113">-AccountName</span></span>
<span data-ttu-id="4119f-114">Имя учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4119f-114">Azure Storage account name.</span></span>
<span data-ttu-id="4119f-115">Например: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="4119f-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="4119f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4119f-116">-DefaultProfile</span></span>
<span data-ttu-id="4119f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4119f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4119f-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="4119f-118">-MountPath</span></span>
<span data-ttu-id="4119f-119">Путь в контейнере, где будет обначена указанное shareName</span><span class="sxs-lookup"><span data-stu-id="4119f-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="4119f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4119f-120">-Name</span></span>
<span data-ttu-id="4119f-121">Идентификатор свойства "Хранилище Azure".</span><span class="sxs-lookup"><span data-stu-id="4119f-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="4119f-122">Должен быть уникальным в пределах веб-приложения или слота</span><span class="sxs-lookup"><span data-stu-id="4119f-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="4119f-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4119f-123">-ShareName</span></span>
<span data-ttu-id="4119f-124">Имя области для крепления к контейнеру</span><span class="sxs-lookup"><span data-stu-id="4119f-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="4119f-125">-Type</span><span class="sxs-lookup"><span data-stu-id="4119f-125">-Type</span></span>
<span data-ttu-id="4119f-126">Тип учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4119f-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="4119f-127">Контейнеры Windows поддерживают только файлы Azure</span><span class="sxs-lookup"><span data-stu-id="4119f-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="4119f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4119f-128">-Confirm</span></span>
<span data-ttu-id="4119f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4119f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4119f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4119f-130">-WhatIf</span></span>
<span data-ttu-id="4119f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4119f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4119f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4119f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4119f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4119f-133">CommonParameters</span></span>
<span data-ttu-id="4119f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4119f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4119f-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4119f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4119f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4119f-136">INPUTS</span></span>

### <span data-ttu-id="4119f-137">Нет</span><span class="sxs-lookup"><span data-stu-id="4119f-137">None</span></span>

## <span data-ttu-id="4119f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4119f-138">OUTPUTS</span></span>

### <span data-ttu-id="4119f-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="4119f-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="4119f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4119f-140">NOTES</span></span>

## <span data-ttu-id="4119f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4119f-141">RELATED LINKS</span></span>
