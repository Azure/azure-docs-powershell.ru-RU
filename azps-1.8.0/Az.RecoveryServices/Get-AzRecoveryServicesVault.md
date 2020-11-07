---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729681"
---
# <span data-ttu-id="a1c5f-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1c5f-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="a1c5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c5f-103">Получает список хранилищ служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="a1c5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1c5f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1c5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1c5f-105">DESCRIPTION</span></span>
<span data-ttu-id="a1c5f-106">Командлет **Get-AzRecoveryServicesVault** получает список хранилищ служб восстановления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="a1c5f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1c5f-107">EXAMPLES</span></span>

### <span data-ttu-id="a1c5f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1c5f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="a1c5f-109">Получение списка хранилищ в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="a1c5f-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a1c5f-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="a1c5f-111">Получение списка хранилищ в группе ресурсов в выбранной подписке.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="a1c5f-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a1c5f-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="a1c5f-113">Получение хранилища в группе ресурсов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="a1c5f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1c5f-114">PARAMETERS</span></span>

### <span data-ttu-id="a1c5f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c5f-115">-DefaultProfile</span></span>
<span data-ttu-id="a1c5f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c5f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1c5f-117">-Name</span></span>
<span data-ttu-id="a1c5f-118">Указывает имя хранилища для запроса.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-118">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="a1c5f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c5f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1c5f-120">Указывает имя группы ресурсов Azure, в которой нужно создать или из которой нужно получить указанный объект служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="a1c5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c5f-121">CommonParameters</span></span>
<span data-ttu-id="a1c5f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1c5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c5f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c5f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c5f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1c5f-124">INPUTS</span></span>

### <span data-ttu-id="a1c5f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a1c5f-125">None</span></span>

## <span data-ttu-id="a1c5f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1c5f-126">OUTPUTS</span></span>

### <span data-ttu-id="a1c5f-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a1c5f-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a1c5f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1c5f-128">NOTES</span></span>

## <span data-ttu-id="a1c5f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1c5f-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1c5f-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a1c5f-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a1c5f-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1c5f-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="a1c5f-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1c5f-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


