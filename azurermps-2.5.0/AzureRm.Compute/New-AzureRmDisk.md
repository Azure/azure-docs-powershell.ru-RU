---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 2cb1cad343f57f164529e3607c1ad0b1ec74df05
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913490"
---
# <span data-ttu-id="1b2a8-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="1b2a8-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="1b2a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2a8-103">Создание управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b2a8-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2a8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2a8-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2a8-106">Командлет **New-AzureRmDisk** создает управляемый диск.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="1b2a8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b2a8-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2a8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b2a8-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="1b2a8-109">Первая команда создает локальный пустой объект диска с размером 5GB в Standard_LRS типе учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="1b2a8-110">Она также задает тип операционной системы Windows и включает параметры шифрования.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="1b2a8-111">Вторая и третья команды устанавливают параметры ключа шифрования диска и ключа шифрования для объекта диска.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="1b2a8-112">Последняя команда принимает объект диска и создает диск с именем "Disk01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1b2a8-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1b2a8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b2a8-113">PARAMETERS</span></span>

### <span data-ttu-id="1b2a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b2a8-114">-AsJob</span></span>
<span data-ttu-id="1b2a8-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2a8-116">-DefaultProfile</span></span>
<span data-ttu-id="1b2a8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-118">-Диск</span><span class="sxs-lookup"><span data-stu-id="1b2a8-118">-Disk</span></span>
<span data-ttu-id="1b2a8-119">Указывает локальный дисковый объект.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1b2a8-120">-DiskName</span></span>
<span data-ttu-id="1b2a8-121">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-121">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b2a8-123">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b2a8-124">-Confirm</span></span>
<span data-ttu-id="1b2a8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2a8-126">-WhatIf</span></span>
<span data-ttu-id="1b2a8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2a8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2a8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2a8-129">CommonParameters</span></span>
<span data-ttu-id="1b2a8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2a8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2a8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2a8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b2a8-132">INPUTS</span></span>

### <span data-ttu-id="1b2a8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1b2a8-133">System.String</span></span>
<span data-ttu-id="1b2a8-134">Microsoft. Azure. Management. COMPUTE. Models.</span><span class="sxs-lookup"><span data-stu-id="1b2a8-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="1b2a8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2a8-135">OUTPUTS</span></span>

### <span data-ttu-id="1b2a8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="1b2a8-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="1b2a8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b2a8-137">NOTES</span></span>

## <span data-ttu-id="1b2a8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b2a8-138">RELATED LINKS</span></span>

