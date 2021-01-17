---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408951"
---
# <span data-ttu-id="68764-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="68764-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="68764-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68764-102">SYNOPSIS</span></span>
<span data-ttu-id="68764-103">Создание сопоставления дисков</span><span class="sxs-lookup"><span data-stu-id="68764-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="68764-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68764-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="68764-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68764-105">DESCRIPTION</span></span>
<span data-ttu-id="68764-106">С New-AzMigrateDiskMapping создается сопоставление с исходным диском, подключенным к серверу, который нужно перенести.</span><span class="sxs-lookup"><span data-stu-id="68764-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="68764-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68764-107">EXAMPLES</span></span>

### <span data-ttu-id="68764-108">Пример 1. Диски</span><span class="sxs-lookup"><span data-stu-id="68764-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="68764-109">Получить объект дисков для ввода данных для New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="68764-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="68764-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68764-110">PARAMETERS</span></span>

### <span data-ttu-id="68764-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="68764-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="68764-112">Определяет набор используемых encyption диска.</span><span class="sxs-lookup"><span data-stu-id="68764-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="68764-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="68764-113">-DiskID</span></span>
<span data-ttu-id="68764-114">Определяет, как будет перенесен диск, вложенный в обнаруженный сервер.</span><span class="sxs-lookup"><span data-stu-id="68764-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="68764-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="68764-115">-DiskType</span></span>
<span data-ttu-id="68764-116">Определяет тип дисков, используемых для Azure VM.</span><span class="sxs-lookup"><span data-stu-id="68764-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68764-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="68764-117">-IsOSDisk</span></span>
<span data-ttu-id="68764-118">Указывает, содержит ли диск операционную систему для переносимого сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="68764-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="68764-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68764-119">CommonParameters</span></span>
<span data-ttu-id="68764-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68764-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68764-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68764-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68764-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68764-122">INPUTS</span></span>

## <span data-ttu-id="68764-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68764-123">OUTPUTS</span></span>

### <span data-ttu-id="68764-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="68764-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="68764-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68764-125">NOTES</span></span>

<span data-ttu-id="68764-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="68764-126">ALIASES</span></span>

## <span data-ttu-id="68764-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68764-127">RELATED LINKS</span></span>

