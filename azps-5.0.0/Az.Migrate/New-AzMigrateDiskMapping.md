---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248869"
---
# <span data-ttu-id="552a0-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="552a0-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="552a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="552a0-102">SYNOPSIS</span></span>
<span data-ttu-id="552a0-103">Создание нового сопоставления дисков</span><span class="sxs-lookup"><span data-stu-id="552a0-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="552a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="552a0-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="552a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="552a0-105">DESCRIPTION</span></span>
<span data-ttu-id="552a0-106">Командлет New-AzMigrateDiskMapping создает сопоставление исходного диска, подключенного к серверу, который необходимо перенести.</span><span class="sxs-lookup"><span data-stu-id="552a0-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="552a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="552a0-107">EXAMPLES</span></span>

### <span data-ttu-id="552a0-108">Пример 1: Создание дисков</span><span class="sxs-lookup"><span data-stu-id="552a0-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="552a0-109">Получение объекта Disks для ввода данных New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="552a0-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="552a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="552a0-110">PARAMETERS</span></span>

### <span data-ttu-id="552a0-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="552a0-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="552a0-112">Указывает используемый дисковый encyption.</span><span class="sxs-lookup"><span data-stu-id="552a0-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="552a0-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="552a0-113">-DiskID</span></span>
<span data-ttu-id="552a0-114">Указывает идентификатор диска, подключенного к обнаруженному серверу, который необходимо перенести.</span><span class="sxs-lookup"><span data-stu-id="552a0-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="552a0-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="552a0-115">-DiskType</span></span>
<span data-ttu-id="552a0-116">Указывает тип дисков, которые будут использоваться для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="552a0-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="552a0-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="552a0-117">-IsOSDisk</span></span>
<span data-ttu-id="552a0-118">Указывает, содержит ли диск операционную систему для исходного сервера.</span><span class="sxs-lookup"><span data-stu-id="552a0-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="552a0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="552a0-119">CommonParameters</span></span>
<span data-ttu-id="552a0-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="552a0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="552a0-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="552a0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="552a0-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="552a0-122">INPUTS</span></span>

## <span data-ttu-id="552a0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="552a0-123">OUTPUTS</span></span>

### <span data-ttu-id="552a0-124">Microsoft. Azure. PowerShell. командлеты. remigrate. Models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="552a0-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="552a0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="552a0-125">NOTES</span></span>

<span data-ttu-id="552a0-126">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="552a0-126">ALIASES</span></span>

## <span data-ttu-id="552a0-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="552a0-127">RELATED LINKS</span></span>

