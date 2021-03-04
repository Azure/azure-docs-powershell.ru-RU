---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982776"
---
# <span data-ttu-id="e5b31-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="e5b31-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="e5b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5b31-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b31-103">Создание сопоставления дисков</span><span class="sxs-lookup"><span data-stu-id="e5b31-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="e5b31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e5b31-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5b31-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5b31-105">DESCRIPTION</span></span>
<span data-ttu-id="e5b31-106">С New-AzMigrateDiskMapping создается сопоставление с исходным диском, подключенным к серверу, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="e5b31-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="e5b31-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e5b31-107">EXAMPLES</span></span>

### <span data-ttu-id="e5b31-108">Пример 1. Диски</span><span class="sxs-lookup"><span data-stu-id="e5b31-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="e5b31-109">Получить объект дисков для ввода данных для New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="e5b31-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="e5b31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5b31-110">PARAMETERS</span></span>

### <span data-ttu-id="e5b31-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="e5b31-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="e5b31-112">Определяет набор используемых encyption диска.</span><span class="sxs-lookup"><span data-stu-id="e5b31-112">Specifies the disk encyption set to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5b31-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="e5b31-113">-DiskID</span></span>
<span data-ttu-id="e5b31-114">Определяет, как будет перенесен диск, вложенный в обнаруженный сервер.</span><span class="sxs-lookup"><span data-stu-id="e5b31-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="e5b31-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="e5b31-115">-DiskType</span></span>
<span data-ttu-id="e5b31-116">Определяет тип дисков, используемых для Azure VM.</span><span class="sxs-lookup"><span data-stu-id="e5b31-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="e5b31-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="e5b31-117">-IsOSDisk</span></span>
<span data-ttu-id="e5b31-118">Указывает, содержит ли диск операционную систему для переносимого сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="e5b31-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="e5b31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b31-119">CommonParameters</span></span>
<span data-ttu-id="e5b31-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5b31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b31-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5b31-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b31-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b31-122">INPUTS</span></span>

## <span data-ttu-id="e5b31-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e5b31-123">OUTPUTS</span></span>

### <span data-ttu-id="e5b31-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="e5b31-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="e5b31-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e5b31-125">NOTES</span></span>

<span data-ttu-id="e5b31-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e5b31-126">ALIASES</span></span>

## <span data-ttu-id="e5b31-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5b31-127">RELATED LINKS</span></span>

