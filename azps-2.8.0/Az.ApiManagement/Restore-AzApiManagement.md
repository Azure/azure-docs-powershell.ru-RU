---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: aa9049489b5a4c28015c208998dae535f514e8f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727961"
---
# <span data-ttu-id="3f49e-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="3f49e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f49e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f49e-103">Восстанавливает службу управления API из указанного блоба хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f49e-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="3f49e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f49e-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f49e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f49e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f49e-106">Командлет **RESTORE-AzApiManagement** восстанавливает службу управления API из указанного резервного копирования, расположенного в большом двоичном объекте Azurestorage.</span><span class="sxs-lookup"><span data-stu-id="3f49e-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="3f49e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f49e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f49e-108">Пример 1: восстановление службы управления API</span><span class="sxs-lookup"><span data-stu-id="3f49e-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="3f49e-109">Эта команда восстанавливает службу управления API из большого двоичного объекта хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f49e-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="3f49e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f49e-110">PARAMETERS</span></span>

### <span data-ttu-id="3f49e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f49e-111">-DefaultProfile</span></span>
<span data-ttu-id="3f49e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f49e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f49e-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f49e-113">-Name</span></span>
<span data-ttu-id="3f49e-114">Указывает имя экземпляра управления API, который будет восстановлен вместе с резервной копией.</span><span class="sxs-lookup"><span data-stu-id="3f49e-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f49e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f49e-115">-PassThru</span></span>
<span data-ttu-id="3f49e-116">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3f49e-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f49e-117">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3f49e-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f49e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f49e-118">-ResourceGroupName</span></span>
<span data-ttu-id="3f49e-119">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="3f49e-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f49e-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="3f49e-120">-SourceBlobName</span></span>
<span data-ttu-id="3f49e-121">Указывает имя блоба источника резервного копирования хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f49e-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f49e-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="3f49e-122">-SourceContainerName</span></span>
<span data-ttu-id="3f49e-123">Указывает имя контейнера источника резервной копии хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="3f49e-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f49e-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3f49e-124">-StorageContext</span></span>
<span data-ttu-id="3f49e-125">Указывает контекст подключения к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="3f49e-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f49e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f49e-126">CommonParameters</span></span>
<span data-ttu-id="3f49e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f49e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f49e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f49e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f49e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f49e-129">INPUTS</span></span>

### <span data-ttu-id="3f49e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3f49e-130">System.String</span></span>

## <span data-ttu-id="3f49e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f49e-131">OUTPUTS</span></span>

### <span data-ttu-id="3f49e-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3f49e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f49e-133">NOTES</span></span>

## <span data-ttu-id="3f49e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f49e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f49e-135">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="3f49e-136">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="3f49e-137">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="3f49e-138">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3f49e-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


