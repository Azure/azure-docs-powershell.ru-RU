---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076260"
---
# <span data-ttu-id="cd38e-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cd38e-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="cd38e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd38e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd38e-103">Импорт файла параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="cd38e-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="cd38e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd38e-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cd38e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd38e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd38e-106">Командлет **Import-AzureSiteRecoveryVaultSettingsFile** импортирует файл параметров хранилища Azure Site Recovery, чтобы настроить контекст хранилища для последующих операций восстановления сайта в текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="cd38e-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="cd38e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd38e-107">EXAMPLES</span></span>

### <span data-ttu-id="cd38e-108">Пример 1: импорт файла параметров хранилища</span><span class="sxs-lookup"><span data-stu-id="cd38e-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="cd38e-109">Эта команда импортирует файл параметров хранилища по указанному пути.</span><span class="sxs-lookup"><span data-stu-id="cd38e-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="cd38e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd38e-110">PARAMETERS</span></span>

### <span data-ttu-id="cd38e-111">-Path</span><span class="sxs-lookup"><span data-stu-id="cd38e-111">-Path</span></span>
<span data-ttu-id="cd38e-112">Задает путь к файлу параметров хранилища для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="cd38e-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="cd38e-113">Этот файл можно скачать на портале хранилища для восстановления сайта и сохранить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="cd38e-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd38e-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="cd38e-114">-Profile</span></span>
<span data-ttu-id="cd38e-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cd38e-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd38e-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cd38e-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd38e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd38e-117">CommonParameters</span></span>
<span data-ttu-id="cd38e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd38e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd38e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd38e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd38e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd38e-120">INPUTS</span></span>

## <span data-ttu-id="cd38e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd38e-121">OUTPUTS</span></span>

## <span data-ttu-id="cd38e-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd38e-122">NOTES</span></span>

## <span data-ttu-id="cd38e-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd38e-123">RELATED LINKS</span></span>

[<span data-ttu-id="cd38e-124">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="cd38e-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="cd38e-125">Get-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="cd38e-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


